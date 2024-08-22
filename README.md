Here's a `README.md` file for setting up your Flask application on `web-01`. This guide will help you with cloning the AirBnB clone repository, configuring the Flask application, and testing it.

---

# AirBnB Clone v2 - Web Framework Setup

## Overview

This document provides instructions to set up the Flask application for the AirBnB clone project on `web-01`. The Flask app will be served from the route `/airbnb-onepage/` on port 5000.

## Requirements

1. Ensure that task #3 of your SSH project is completed for `web-01`.
2. Install the `net-tools` package:
   ```bash
   sudo apt install -y net-tools
   ```

## Setup Instructions

### 1. Clone the Repository

SSH into `web-01` and clone your AirBnB clone repository:

```bash
git clone https://github.com/your-username/alx-system_engineering-devops.git
```

Navigate to the project directory:

```bash
cd alx-system_engineering-devops/0x1A-application_server
```

### 2. Configure Flask Application

1. **Navigate to the Flask Application Directory**

   Go to the directory containing your Flask application:
   
   ```bash
   cd web_flask
   ```

2. **Edit `0-hello_route.py`**

   Open `0-hello_route.py` in a text editor and ensure it is set up to serve its content from the `/airbnb-onepage/` route on port 5000. Your `0-hello_route.py` should look like this:

   ```python
   from flask import Flask
   
   app = Flask(__name__)

   @app.route('/airbnb-onepage/')
   def hello():
       return "Hello HBNB!"

   if __name__ == "__main__":
       app.run(host='0.0.0.0', port=5000)
   ```

   Make sure the `Flask` app object is named `app`.

### 3. Run the Flask Application

Execute the Flask application using the following command:

```bash
python3 -m web_flask.0-hello_route
```

You should see output similar to:

```
 * Serving Flask app "0-hello_route" (lazy loading)
 * Environment: production
   WARNING: Do not use the development server in a production environment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
```

### 4. Verify the Setup

1. **Check the Application Locally**

   Open another terminal window and use `curl` to test the application:

   ```bash
   curl 127.0.0.1:5000/airbnb-onepage/
   ```

   You should receive the response:

   ```
   Hello HBNB!
   ```

## Repository Information

- **GitHub Repository**: [alx-system_engineering-devops](https://github.com/your-username/alx-system_engineering-devops)
- **Directory**: `0x1A-application_server`
- **File**: `README.md`

## Notes

- Ensure that your Flask application object is named `app` to comply with the requirements for checking your code.
- The development server should only be used for testing purposes. For production, consider using a WSGI server like Gunicorn.

---

Feel free to adjust the repository URL and any other specific details as needed.
