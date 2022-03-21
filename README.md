# Learning-Understanding-React
Day by Day learning React
## Day 1
General stuff about React and introduction to React.js. React is a Javascript Library but we use React instead of plain JavaScript because it offers advantages such as higher level syntax which makes building complex applications way easier. The usage of many components lets us organize our code in a more elegant and efficient way.  
Throughout a span of 15-20 days i will focus on basics and foundations introducing key features firstly, then move on to more advanced concepts while building small apps.  
- Basics  
1. Components & building UIs
2. Working with Events & Data: "props" and "state"
3. Styling React Apps & Components
4. Introduction to "Hooks"
- Advanced
1. Side Effects, "Refs" & more React Hooks
2. React's Context API & Redux
3. Forms, Http Requests & "Custom Hooks"
4. Routing, Deployment NextJs & more     
Start by setting up the enviroment of Visual Studio Code using some extensions as well including(Prettier, Material Icon Theme, Es7+ Snippets)
and reviewing JavaScript Fundamentals such as Modules, Arrow Functions, Classes, Array functions  
## Day 2  
Start by creating a new React project using Visual Studio Code. In order to create it i will need to download node.js and install the enviroment of create-react-app.  
After using the commands npm install and npm run on the terminal the rpoject is ready to go. Firstly i'm clearing the source folder with all the unnecessary files.  
An important note here is that the Index.js file in the source folder is the first file to be executed.  
Another important note is the JSX extension in react which is HTML code inside JavaScript. JSX stands for JavaScriptXML and it makes it easier for us to write and add HTML in React.  
React is all about components and how they interact with each other. The first component that i came across is in the index.js file  
![Screenshot_1](https://user-images.githubusercontent.com/90603989/157984609-9a3e2934-d5bf-4d99-9ab5-c5aef16baaed.png)  
If we go then to App.js i will find out that ***a component in react is just a Javascript function.***   
I will create my custom component next and generally it is better to put new components in to new files so that you know where everything is and organize your interface more efficiently.  
After creating a new folder and file embedded in it my custom component looks like this  
![Screenshot_2](https://user-images.githubusercontent.com/90603989/157987363-afa94d11-76e1-41e1-9284-b94c617f96f6.png)  
After exporting it, i have to import in in App.js and inside the function taking care for the component to start with capital letter because it is custom made  
![Screenshot_3](https://user-images.githubusercontent.com/90603989/157987366-049b139e-dabf-4010-bc22-4d1bf19bd7f1.png)  
## Day 3  
To make my component more complex i will try to make it show the amount and the date as well, writing HTML code. ***An important rule here is that in React you must have only 1 root element per return statement.*** In order to bypass this rule we can wrap our existing div in another div. Adding brackets to make my code more clear the component looks like that. ![Screenshot_1](https://user-images.githubusercontent.com/90603989/158228168-f0530dc0-9d9a-496d-a507-2783200b57fd.png)  
Now in order to style add basic Css styling i will create a new file in the components folder naming it ExpenseItem.css and copy paste the code from a Github link.The ExpenseItem.css file looks like this. ![Screenshot_2](https://user-images.githubusercontent.com/90603989/158228174-b6575852-9580-453f-a7f7-6842340a51ff.png) In order although for React to conclude this file, i must import it in the ExpenseItem.js so that React knows that the Css file must be considered. In the Css files though there are Css classes which will be added to elements so that they have a certain look. In the ExpenseItem.js file when i add the Css classes, ***it is important to remember that when adding classes it's not HTML code, instead its the special JSX syntax that React has therefore i do not write class, i use className.*** The ExpenseItem.js then looks this way ![Screenshot_3](https://user-images.githubusercontent.com/90603989/158228162-9bcaf62d-7112-4e52-a728-08683ea14ffe.png)  
In the ExpenseItem.js i will write JavaScript so as to fake data that a user might give us. Creating some const variables and using the Date constructor straight from JavaScript i now have the data/values that i need to get to the HTML code. The next step is to turn all this raw handwriten code into Dynamic Data with the goal of making it reusable so that we can take advantage of it in other cases as well. The way to output dynamic data inside of JSX snippets are the curly braces {} which is given by React's special syntax. Inside these curly braces i can run basic Javascript Expressions for example {1+1}. Inside these curly braces i can refer to the value stored in the previous constants. Although in the date const i have to replace it with .toISOSstring() so that it doesnt produce an error on the screen.The file then comes up like this ![Screenshot_4](https://user-images.githubusercontent.com/90603989/158228166-3b424adf-3985-4adb-b7e0-57e80ef2ca73.png)  
## Day 4  
The focus of today will be to make components reusable and passing data via Props(Properties). Components can't just use data stored in other components so i am gonna utilize the Props or attributes to bypass that. In App.js i create multiple objects in the expenses array which i got from github as well and i will assign values to attributes using curly braces, accessing the expense items. The App.js looks like this ![Screenshot_2](https://user-images.githubusercontent.com/90603989/158268195-84487516-5636-4e84-aeed-5adc314854f9.png)  
After that i have to go to ExpenseItem.js and use the prop as a parameter in the ExpenseItem function which will act as an object which holds all the received attributes as properties.***Reminder that the key which you access on your props object has to be the name you picked for your attribute.*** Now the ExpenseItem.js looks like this ![Screenshot_1](https://user-images.githubusercontent.com/90603989/158268190-5f1a7a7d-625d-4430-9d45-4f5985038aa0.png)  
And now it runs smoothly  
![Screenshot_3](https://user-images.githubusercontent.com/90603989/158268185-b521c04a-9a83-4a06-aab1-4d6dcc2837ce.png)  
## Day 5  
The next step is to make adjustments so that day,year,month appear more elegantly on the screen. By adding normal JavaScript logic to components, using props and making use of toLocaleString my ExpenseItem.js file looks like this ![Screenshot_1](https://user-images.githubusercontent.com/90603989/158408579-f60e0d4a-1f40-4979-99ac-7e3ae62afdfd.png)  
In order now to make my date/calendar a seperate component so as to split the ExpenseItem into multiple components i will create a new component named ExpenseDate.js. The goal here is to split into multiple components so that it is easier to manipulate my code. By creating a new custom component(function) and giving it appropriate styling the files look like this. ![Screenshot_2](https://user-images.githubusercontent.com/90603989/158415997-1133c5f5-d209-4ab5-8271-445ce50be544.png)  
![Screenshot_3](https://user-images.githubusercontent.com/90603989/158415986-043f6b86-fbf8-4ee9-bc3b-521f561d8ce0.png)  
## Day 6  
I will create another 4 components which include Expenses.js,Expenses.css,Card.js,Card.css. The goal is to create many reusable components so that we structure our user interface which is also called Composition. The Card.js component can act as a shell or a container for the ExpenseItem.js or the Expenses.js files and i can replace their opening div's with the Card component i just created. Although normally that could not work, React gives me this option by the use of {props.children} prop. ***Children is a reserved name and the value of this 'special' prop will always be the content between the opening and closing tags of my custom component.*** Now i want to make sure that a className can be set on the Card(custom) component. I have to add a classes constant inside the function Card which will look like this.
![Screenshot_1](https://user-images.githubusercontent.com/90603989/158907330-d42cbf25-b98d-4d77-bc0d-68399c9b897c.png)  
The files of Expenses.js,Expenses.css and Card.css are as following
![Screenshot_2](https://user-images.githubusercontent.com/90603989/158907332-2c516a16-6dd6-4330-b78f-97bca3dd7a1d.png)
![Screenshot_4](https://user-images.githubusercontent.com/90603989/158907326-4dc4de82-a3a9-4ef9-8d63-eed8b7b5f174.png)
![Screenshot_3](https://user-images.githubusercontent.com/90603989/158907318-1846e408-137f-4c60-90ed-d0b3cc643cd3.png)  
The final result works and in my screen i can see this as intended.
![Screenshot_5](https://user-images.githubusercontent.com/90603989/158907329-7a501b1a-263c-4884-8076-eb6db79f6a18.png)  
## Day 7  
All the custom components that i used so far are just JSX code and do not appear on the web page if i inspect it. There is only HTML code(elements). When i use JSX i call the React.createElement method. In the past we needed to import React from 'react' in all React component files, or at least in every file that we used JSX. The modern React projects do that by default so i dont need to do it by myself. I am commenting the React.createElement method in App.js. Another thing is that if a project gets bigger with time i will need to organize my component files better using more folders and subfolders. I need to be careful though because when you move files into subfolders you have to adjust the imports on the files so that they match your new layout. In this current project i will create an Expenses and a UI subfolders moving Card,js, Card.css into UI and Expenses,ExpenseDate,ExpenseItem(.js,css) into Expenses subfolder. After adjusting the imports in App.js, Expenses.js and ExpenseItem.js the final output looks way more readable and easy to figure out where everthing is located. One last thing is that i can replace the functions in my project with Arrow functions because they are used by many people and it is nice to know that it can work this way too.
![Screenshot_2](https://user-images.githubusercontent.com/90603989/159127705-bd15cd60-7ad5-47de-b7a4-1e1ad7fd7599.png)  
## Day 8
I will begin now to work with events, updating the UI and work with "State". In the ExpenseItem.js file i will create a button, simple to begin with and it will put out on my screen a simple "Change the Title". In order now to add an event listener to the JSX element (the button i created) i will add inside the button a special prop which will set a value for this button and it will start with on(...). I will use the onClick so as to start with which is an event listener on click events for my button. I must also issue a value for the onClick which will be a ***function***. After creating the clickHandler function my code looks like this   
![Screenshot_1](https://user-images.githubusercontent.com/90603989/159312134-1707f97e-bc39-413d-8c4a-6e19266b3e25.png)  
In order to understand better how component functions are executed i will tweak my code a bit so that i can see Updated on my Dev Tools console.
![Screenshot_2](https://user-images.githubusercontent.com/90603989/159335305-18c79801-9b40-4b9d-b38d-e0afa098e4b8.png)



