# Application Server

This project involved deploying our AirBnB clone as part of the ALX program. The objective was to configure Nginx on the provided web servers to serve a WSGI Flask application running via Gunicorn. Additionally, I set up an Upstart script to ensure the application would automatically restart after a server reboot.

## Tasks :page_with_curl:

### 1. **Set Up Development with Python**
   - **File:** `web_flask/0-hello_route.py`
   - **Description:** Configured this file from the [AirBnB_clone_v2](https://github.com/Bennyonye/AirBnB_clone_v2) project to serve content on the route `/airbnb-onepage/`, running on port `5000`.

### 2. **Set Up Production with Gunicorn**
   - **Description:** Set up a production environment by installing and configuring Gunicorn to serve the same file from task 1.

### 3. **Serve a Page with Nginx**
   - **File:** [2-app_server-nginx_config](./2-app_server-nginx_config)
   - **Description:** Created an Nginx configuration file to proxy requests on the route `/airbnb-onepage/` to the Gunicorn app running on port `5000`.

### 4. **Add a Route with Query Parameters**
   - **File:** [3-app_server-nginx_config](./3-app_server-nginx_config)
   - **Description:** Modified the Nginx configuration to proxy requests on the route `/airbnb-dynamic/number_odd_or_even/<int:num>` to the Gunicorn app.

### 5. **Set Up Your API**
   - **File:** [4-app_server-nginx_config](./4-app_server-nginx_config)
   - **Description:** Configured the API from the [AirBnB_clone_v3](https://github.com/Tijani1402/AirBnB_clone_v31) project to run on Gunicorn and be served through Nginx.

### 6. **Serve Your AirBnB Clone**
   - **File:** [5-app_server-nginx_config](./5-app_server-nginx_config)
   - **Description:** Configured the full AirBnB app from [AirBnB_clone_v4](https://github.com/aysuarex/AirBnB_clone_v4) to run on Gunicorn and be served through Nginx, including serving static assets from `web_dynamic/static/`.

### 7. **Deploy It**
   - **File:** [gunicorn.conf](./gunicorn.conf)
   - **Description:** Created an Upstart script configuration to start a Gunicorn process bound to port 5003. This configuration spawns three worker processes and logs errors to `/tmp/airbnb-error.log` and access logs to `/tmp/airbnb-access.log`.

### 8. **No Service Interruption**
   - **File:** [4-reload_gunicorn_no_downtime](./4-reload_gunicorn_no_downtime)
   - **Description:** Developed a Bash script to gracefully reload Gunicorn, ensuring no downtime during the reload process.
