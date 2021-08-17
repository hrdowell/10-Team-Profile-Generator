# 10 Object-Oriented Programming: Team Profile Generator



### About

The Team Profile Generator is a Node.js command-line application that takes in information about engineering employees, then creates an HTML webpage that displays profile summaries for each person.

- Github Profile: http://github.com/hrdowell
- Github Repository: http://github/hrdowell/10-Team-Profile-Generator
  - index.html in the dist repository contains a sample HTML file. 
- Github Pages: https://hrdowell.github.io/10-Team-Profile-Generator/





#### User Story

```md
AS A manager
I WANT to generate a webpage that displays my team's basic info
SO THAT I have quick access to their emails and GitHub profiles
```



#### Acceptance Criteria

```md
GIVEN a command-line application that accepts user input
WHEN I am prompted for my team members and their information
THEN an HTML file is generated that displays a nicely formatted team roster based on user input
WHEN I click on an email address in the HTML
THEN my default email program opens and populates the TO field of the email with the address
WHEN I click on the GitHub username
THEN that GitHub profile opens in a new tab
WHEN I start the application
THEN I am prompted to enter the team manager’s name, employee ID, email address, and office number
WHEN I enter the team manager’s name, employee ID, email address, and office number
THEN I am presented with a menu with the option to add an engineer or an intern or to finish building my team
WHEN I select the engineer option
THEN I am prompted to enter the engineer’s name, ID, email, and GitHub username, and I am taken back to the menu
WHEN I select the intern option
THEN I am prompted to enter the intern’s name, ID, email, and school, and I am taken back to the menu
WHEN I decide to finish building my team
THEN I exit the application, and the HTML is generated
```





#### Installation

Please install the node packages INQUIRER in your terminal  to use this application.

In order to run tests on the application, install the JEST package, and run `npm run test`  from the terminal.

```
npm install inquirer
npm install jest
```



#### Usage

Clone the above 10-Team-Generator repo and install the node packages listed above (inquirer and jest). Use the command line to navigate to the root of the application (index.js) and open in the integrated terminal. Run node index.js in the terminal. Follow the prompts in order to add team members and their information to your roster. Only one manager can be added per team. When finished, your team roster will be generated onto a new webpage called team.html located in the src folder that can be opened in the browser.



#### Video Demo

Click here to see a demo of this project in action: https://vimeo.com/588180988.



#### Screenshots

![Terminal Screenshot](C:\Users\Hannah\Documents\GitHub\10-Team-Profile-Generator\assets\terminal.PNG)

As pictured, the application runs from the terminal using node. 



![Screenshot of Browser](C:\Users\Hannah\Documents\GitHub\10-Team-Profile-Generator\assets\webpage.PNG)

Here is the example of the generated Team Profile Roster from the demo video.



* 

## Review

You are required to submit the following for review:

* A walkthrough video that demonstrates the functionality of the application and passing tests.

* A sample HTML file generated using your application.

* The URL of the GitHub repository, with a unique name and a readme describing the project.

---
© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.
-----------------------------------------------
# Team-Profile-Generator
Unit 10 homework

# Project Description
The Team Profile Generator is a command-line-input application run in Node that requests information from the user about members of an engineering team and generates an HTML file displaying that information.  Before running the application the user must perform an npm install to install all required dependencies.

Upon launching the app, the user is asked to describe the first member of their team.  The user enters the team member's name, selects that member's role from a list (options include "Engineer," "Intern," and "Manager), enters the member's ID (any string), enters the member's email address, and then must enter another piece of information that will differ depending on what role was selected.  If "Engineer" was selected, the app asks the user for the team member's GitHub username; if "Intern" was selected, the member's school is requested; and if "Manager" was chosen, the user is prompted for the team member's phone number.

A screenshot showing an example user input is shown below:

![Screenshot of user input](https://github.com/hrdowell/10-Team-Profile-Generator/blob/master/assets/images/terminal-screenshot.JPG)

When all information on the team member has been entered, the user is asked whether there are any more members they would like to add.  If so, the user is asked the same questions about the new team member.  If not, an HTML file is created with cards displaying the information on all the team members entered by the user in the "outputs" folder titled "team.html."  A screenshot of an example team profile is shown below:

![Screenshot of HTML output](https://github.com/hrdowell/10-Team-Profile-Generator/blob/master/assets/images/html-screenshot.JPG)

# Techniques and Technologies Used
This app was created using Object-Oriented Programming concepts, namely using classes and constructors to create "team member" objects based on information entered by the user.  The app is run using Node.js, and uses the "Inquirer" and "FS" node modules.  Files for different objects are also stored in separate .js files and passed among one another using module.exports and require.

This app uses concepts from Test-Driven Development.  Jest is used to perform tests on all the class constructors to ensure that they behave as expected.  The FS node module is used to generate an HTML file from strings written in JavaScript.  Since the app will work no matter how many team members the user adds to the system, the HTML is built in a piecemeal fashion, starting with the head and part of the body.  For each team member object created, a new column with a card inside containing the team member information is added.  Then when the last member has been added, the last bit of the HTML is added to the file.  One complication experienced during this process was that since the fs.appendFile method is asynchronous, the bottom part of the HTML could be added before the HTML containing information on the last team member had been added.  In order to deal with this, the function that adds the team member information to the HTML was converted into a promise, and only once the promise was resolved would the bottom part of the HTML be added to the output file.