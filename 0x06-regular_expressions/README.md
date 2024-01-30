# 0x06-regular_expressions
##### Regex DevOps

## Background Context
For this project, you have to build your regular expression using Oniguruma, a regular expression library that which is used by Ruby by default. Note that other regular expression libraries sometimes have different properties.

Because the focus of this exercise is to play with regular expressions (regex), here is the Ruby code that you should use, just replace the regexp part, meaning the code in between the //:

* sylvain@ubuntu$ cat example.rb
#!/usr/bin/env ruby
puts ARGV[0].scan(/127.0.0.[0-9]/).join
sylvain@ubuntu$
sylvain@ubuntu$ ./example.rb 127.0.0.2
127.0.0.2
sylvain@ubuntu$ ./example.rb 127.0.0.1
127.0.0.1
sylvain@ubuntu$ ./example.rb 127.0.0.a *

## Resources
#### Read or watch:

1. Regular expressions - basics
2. Regular expressions - advanced
3. Rubular is your best friend
4. Use a regular expression against a problem: now you have 2 problems
5. Learn Regular Expressions with simple, interactive exercises

## General Requirements

1. Allowed editors: vi, vim, emacs
2. All your files will be interpreted on Ubuntu 20.04 LTS
3. All your files should end with a new line
4. A README.md file, at the root of the folder of the project, is mandatory
5. All your Bash script files must be executable
6. The first line of all your Bash scripts should be exactly #!/usr/bin/env ruby
7. All your regex must be built for the Oniguruma library

## Tasks

0. Simply matching School: Ensure that;
* the regular expression must match School.
* while using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method.

1. Repetition Token #0:
* find the regular expression that will match the above cases
* while using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

2. Repetition Token #1:
* find the regular expression that will match the above cases
* while using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

3. Repetition Token #2:
* find the regular expression that will match the above cases
* while using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

4. Repetition Token #3:
* find the regular expression that will match the above cases
* while using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method
* ensure the regex does not contain square brackets

5. Not quite HBTN yet: Ensure that;
* the regular expression must be exactly matching a string that starts with h ends with n and can have any single character in between
* while using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

6. Call me maybe: Ensure that;
* the regular expression must match a 10 digit phone number

7. OMG WHY ARE YOU SHOUTING?: Ensure that;
* the regular expression must be only matching: capital letters

8. Textme: a TextMe VoIP Engineer comes to you and explains she wants to run some statistics on the TextMe app text messages transactions.
* our script should output: [SENDER],[RECEIVER],[FLAGS]
  - The sender phone number or name (including country code if present)
  - The receiver phone number or name (including country code if present)
  - The flags that were used

You can find a [log file here].

@BennyOnye
