# Flask-Web-Application-with-Dynamic-URL-Building

## Overview
This project implements a **Flask Web Application** with multiple routes for serving HTML pages, handling form submissions, and demonstrating **dynamic URL building** using variable rules and Jinja2 template engine.

## Features
- **Homepage (`/`)**: Displays a simple welcome message.
- **Index Page (`/index`)**: Serves an `index.html` template.
- **About Page (`/about`)**: Serves an `about.html` template.
- **Form Page (`/form`)**: Handles GET and POST requests for user input.
- **Submit Page (`/submit`)**: Processes form submissions.
- **Dynamic URL Handling**:
  - Uses **Variable Rules** (e.g., `/success/<int:score>`) to process dynamic values.
  - Implements **conditional rendering** based on user input.
- **Jinja2 Templating**:
  - Uses `{{ }}` for expressions.
  - Uses `{% %}` for loops and conditions.
  - `{# #}` for comments.

## Technologies Used
- **Flask**: Lightweight web framework for Python.
- **Jinja2**: Template engine for rendering HTML pages dynamically.
- **HTML & CSS**: Basic front-end structure.

## Implementation Details
- **Flask is initialized** using `Flask(__name__)`.
- **Templates (`.html` files)** are rendered using `render_template()`.
- **Form Handling**:
  - Uses `request.form[]` to retrieve submitted data.
  - Redirects users based on their input.
- **Dynamic URL Routing**:
  - `@app.route('/success/<int:score>')` handles variable-based results.
  - Redirects users dynamically using `url_for()` and `redirect()`.
- **Static Files Support**: CSS and JavaScript files are loaded using `url_for('static', filename='...')`.

## Installation & Usage
### **Setup Instructions**
1. **Install Flask**:
   ```bash
   pip install flask
   ```
2. **Run the Application**:
   ```bash
   python app.py
   ```
3. **Access the Web Pages**:
   - Open `http://127.0.0.1:5000/` in a browser.
   - Navigate to `/index`, `/about`, `/form`, and `/submit`.
   - Test dynamic URLs like `/success/75` or `/success/30`.

## Future Enhancements
- Integrate a **database** to store form submissions.
- Implement **user authentication**.
- Deploy on a cloud platform (AWS, Heroku).
- Expand Jinja2 templates for better UI customization.

## Conclusion
This Flask application serves as a foundation for **dynamic web development**, incorporating **backend logic**, **HTML rendering**, and **URL handling**. It can be expanded into a more complex system with additional functionalities.

