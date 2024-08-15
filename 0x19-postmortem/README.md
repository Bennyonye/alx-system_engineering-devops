# Postmortem

## Incident Summary

On the release date of ALX's System Engineering & DevOps project 0x19, at approximately 06:00 WAT in Nigeria, an outage was detected on an isolated Ubuntu 14.04 container running an Apache web server. The server responded to GET requests with a `500 Internal Server Error` instead of delivering the expected HTML file for a simple Holberton WordPress site.

## Debugging Process

The issue was identified and debugged by Brennan (BDB... yes, that's my initials!). The incident was first noticed around 19:20 PST. Here’s the step-by-step process used to diagnose and resolve the issue:

1. **Process Verification:** Used `ps aux` to check running processes. Two `apache2` processes (`root` and `www-data`) were found running correctly.

2. **Configuration Check:** Inspected the `sites-available` directory in `/etc/apache2/` and confirmed that the web server was serving content from `/var/www/html/`.

3. **System Call Tracing (strace):** Ran `strace` on the PID of the `root` Apache process while curling the server in another terminal. This yielded no useful information.

4. **Further Tracing:** Repeated the `strace` process on the PID of the `www-data` process. This time, an `-1 ENOENT (No such file or directory)` error was observed when trying to access `/var/www/html/wp-includes/class-wp-locale.phpp`.

5. **Error Identification:** Searched through the files in `/var/www/html/` to locate the erroneous `.phpp` file extension. The typo was found in the `wp-settings.php` file on line 137: `require_once( ABSPATH . WPINC . '/class-wp-locale.php' );`.

6. **Correction:** Removed the incorrect trailing `p` from the file extension.

7. **Validation:** Performed another `curl` on the server, which now returned a `200 OK` status.

8. **Automation:** Created a Puppet manifest to automate the correction of this error in the future.

## Summary

The root cause of the outage was a simple typo in the `wp-settings.php` file, where a file was being referenced with an incorrect `.phpp` extension. This prevented WordPress from loading the necessary `class-wp-locale.php` file.

The fix was straightforward: correcting the file extension typo in `wp-settings.php`.

## Prevention Measures

To avoid similar issues in the future, consider the following preventive measures:

1. **Thorough Testing:** Always test the application thoroughly before deployment. This error could have been detected and resolved during pre-deployment testing.

2. **Monitoring:** Implement uptime monitoring using a service like [UptimeRobot](https://uptimerobot.com/) to receive instant alerts in case of an outage.

Additionally, I created a Puppet manifest, [0-strace_is_your_friend.pp](https://github.com/bdbaraban/holberton-system_engineering-devops/blob/master/0x17-web_stack_debugging_3/0-strace_is_your_friend.pp), which automates the correction of any similar typos in the `/var/www/html/wp-settings.php` file by replacing `.phpp` with `.php`.

Of course, this will never happen again—because as developers, we never make mistakes, right? :wink:
