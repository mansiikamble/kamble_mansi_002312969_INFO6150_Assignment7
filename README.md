"# kamble_mansi_002312969_INFO6150_Assignment7" 

*Overview for login page and calculator page* :
This project consists of two HTML pages: a Login Page and a Calculator Page. The Login Page allows users to enter their credentials, while the Calculator Page performs basic arithmetic operations. The application uses jQuery for DOM manipulation and validation.

Files : 
login.html: Contains the login form and validation logic.
calculator.html: Displays a calculator interface for performing arithmetic operations.


*Login Page (login.html)*

Features - 
Form Fields: Inputs for email, username, password, and password confirmation.
Validation: Each input field is validated to ensure correct formats and lengths.
Error Display: Error messages are shown for invalid inputs.
Button State: The "Login" button is disabled until all fields are valid.

Functions - 
validateField(field, errorId, regex, minLen, maxLen):
Validates the input field based on specified criteria (length and format).
Displays error messages if validation fails.
Returns true if valid, otherwise false.

jQuery Usage - 
$(document).ready(...): Ensures the DOM is fully loaded before executing the script.
on('input', ...): Listens for user input in fields to trigger validation.
prop('disabled', ...): Toggles the disabled state of the login button based on validation results.


*Calculator Page* (calculator.html)

Features
Arithmetic Operations: Supports addition, subtraction, multiplication, and division.
Input Validation: Validates that inputs are numbers before performing operations.
Dynamic Result Display: Shows the result of the operation directly on the page.

Functions
validateNumber(field, errorId):
Checks if the input is non-empty and a valid number.
Displays error messages if validation fails.
Returns true if valid, otherwise false.

calculate(num1, num2, operation):
Performs the specified arithmetic operation and returns the result.
Handles division by zero with an appropriate message.

handleOperation(operation):
Validates input fields before performing the calculation.
Displays the result of the operation if inputs are valid.

jQuery Usage
$('#welcomeUser').text(...): Displays the logged-in username.
on('click', ...): Listens for clicks on the operation buttons to trigger calculations.

How to Use
Open login.html in a web browser.
Enter a valid email (ending with @northeastern.edu), username, password, and confirm password.
Click the "Login" button to proceed to the calculator.
On calculator.html, input two numbers and click the desired operation button to see the result.
Dependencies


*Overview for Stopwatch Application* : 
This project is a simple Stopwatch Application built using HTML, CSS, and JavaScript. The application provides a user-friendly interface to start, stop, and reset a stopwatch, displaying the elapsed time in hours, minutes, and seconds. It also includes a date picker to select a date.

Features
Start, Stop, and Reset Buttons: Control the stopwatch with intuitive buttons.
Elapsed Time Display: Shows the elapsed time in HH:MM:SS format.
Date Picker: Allows users to select a date, which defaults to the current date upon loading.

Files
index.html: The main HTML file containing the application.
UI Components
Title: Displays the title "Stopwatch Application".
Time Display: A dedicated area to show the elapsed time.
Buttons:
Start: Begins the stopwatch.
Stop: Pauses the stopwatch.
Reset: Resets the elapsed time to zero.

Code Explanation
HTML Structure
The document is structured with a header, a time display, a date picker input, and control buttons.

CSS Styling
The application uses basic CSS for layout and styling, including:
Flexbox for centering content.
Styling for buttons and the time display to enhance user experience.

JavaScript Functionality

Variables:
timer: Holds the interval ID for the stopwatch.
elapsedSeconds: Tracks the number of seconds elapsed.
timeLabel: References the time display element.

Functions:
updateTimeDisplay(): Updates the time display based on the elapsed seconds, formatting it into HH:MM:SS.
startTimer(): Starts the timer and updates the elapsed seconds every second.
stopTimer(): Stops the timer by clearing the interval.
setCurrentDate(): Sets the date picker to the current date on page load.

Event Listeners :
Event listeners are added to buttons to start, stop, and reset the timer:
Start Button: Initiates the timer when clicked.
Stop Button: Pauses the timer when clicked.
Reset Button: Resets the timer and display when clicked.
On Page Load
The setCurrentDate function is called when the window loads to ensure the date picker is set to today's date.

Key Concepts : 

Promises and Async/Await:
The startTimer and stopTimer functions return Promises, allowing for asynchronous operation handling.
Using async/await in the event listeners simplifies the code and makes it easier to read and manage asynchronous actions.

setInterval():
The setInterval function is used to repeatedly execute a specified function (updating the elapsed time) at defined intervals (every 1000 milliseconds, or 1 second).
This creates a timer that increments the elapsedSeconds variable.

clearInterval():
The clearInterval function is used to stop the timer when the user clicks the "Stop" button or the "Reset" button.
This function takes the timer variable (which holds the interval ID) as an argument to clear the ongoing interval.

How to Use
Open stopwatch.html in a web browser.
Click the "Start" button to begin timing.
Click the "Stop" button to pause the timing.
Click the "Reset" button to reset the timer to zero.
Use the date picker to select a date if desired.