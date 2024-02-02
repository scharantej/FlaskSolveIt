## Flask Application Design: Meet-and-Greet App

### HTML Files

- **index.html**: This file serves as the webpage for the application. It comprises a form that allows users to input their names, submit the information, and provide a greeting based on the submitted name.
- **greeting.html**: This file is responsible for displaying the personalized greeting to the user. It retrieves the submitted name and displays it within a greeting message.

### Routes

- **@app.route('/', methods=['GET', 'POST'])**: This route corresponds to the index page. When a user accesses the root URL ('/'), the application renders the 'index.html' file. Upon submitting the name, a POST request is made to the same route. The submitted name is extracted, and the application redirects to the '/greeting' route with the name as a query parameter.

- **@app.route('/greeting')**: This route handles displaying the greeting. It retrieves the name from the query parameters and passes it to the 'greeting.html' template. The template then displays a customized greeting message to the user.

### Functionality Overview

1. The user accesses the application via the root URL ('/').
2. The 'index.html' file is rendered, presenting a form for the user to enter and submit their name.
3. Upon form submission, a POST request is made to the same route ('/').
4. The application extracts the submitted name from the request payload.
5. The application redirects to the '/greeting' route, passing the name as a query parameter.
6. The 'greeting.html' template is rendered, receiving the name as a template variable.
7. The personalized greeting is displayed to the user based on the submitted name.