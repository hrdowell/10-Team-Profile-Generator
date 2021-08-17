# 10 Object-Oriented Programming: Team Profile Generator



### ✨About

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





#### Installation: Inquirer and Jest Packages Required

📦Please install the node package INQUIRER in your terminal  to use this application. This package is used so that the roster can be filled out in the terminal and generated into a webpage application.

In order to run tests on the application, install the JEST package, and run `npm run test`  from the terminal.

```
npm install inquirer
npm install jest
```



#### Usage

Clone the above 10-Team-Generator repo and install the node packages listed above (inquirer and jest). Use the command line to navigate to the root of the application (index.js) and open in the integrated terminal. Run node index.js in the terminal. Follow the prompts in order to add team members and their information to your roster. Only one manager can be added per team. When finished, your team roster will be generated onto a new webpage called team.html located in the src folder that can be opened in the browser.



#### Video Demo

✨Click here to see a demo of this project in action: https://vimeo.com/588180988.



#### Screenshots

##### ✨Sample HTML file (index.html):

![sample generated index.html file](C:\Users\Hannah\Documents\GitHub\10-Team-Profile-Generator\assets\sample-html-1.PNG)

![(continued) sample generated index.html file](C:\Users\Hannah\Documents\GitHub\10-Team-Profile-Generator\assets\sample-html-2.PNG)

📸The screenshot above shows a sample generated index.html containing user inputs from the terminal.



![Terminal Screenshot](C:\Users\Hannah\Documents\GitHub\10-Team-Profile-Generator\assets\terminal.PNG)

📸As pictured, the application runs from the terminal using node. 



![Screenshot of Browser](C:\Users\Hannah\Documents\GitHub\10-Team-Profile-Generator\assets\webpage.PNG)

💻 Here is an example of the generated Team Profile Roster from the demo video.