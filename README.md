# MERN Workbook
## Provide an overview and description of a standard source control process for a large project:

The source control is a category of software tools that provide stability and sustainability when managing source code for any development project. A version control software like Git helps keep track of every modification to the code stored for each project. The reason software like this is important is that if any code is lost, replaced or broken, the developer can review previous code, see specific changes and even roll back the whole project to an earlier saved version.

### Setting up a Repository
A standard source control project for a large project is usually started by creating a new, empty repository. On Github, this is done by being logged in, selecting the `New` icon next to the `Repositories` title.
![New Repo](https://raw.githubusercontent.com/amberemeny/MERN-Workbook/master/images/newRepo.png)Then, details about the new repository can be added with the option to initialize a `README.md` file upon creation.
![New Repo Details](https://raw.githubusercontent.com/amberemeny/MERN-Workbook/master/images/newRepoDetails.png)Next, after the repo is created, Github will redirect the user to a screen detailing the steps to set up the repository inside the terminal.
![Setup Repo Github](https://raw.githubusercontent.com/amberemeny/MERN-Workbook/master/images/createdRepo.png)Over in the terminal window, create a new folder for the project and enter it. Then, follow the steps in the `...or create a new repository on the command line` section.
Following these steps will create a README file (if one hasn't already been created) and initialize the project folder as a git repository. Initializing the folder as a repo will direct git to set up the associated files for the source control process including the `.git-ignore` file, which essentially flags any recorded files to *not* be uploaded to the Github repo. This becomes useful when using certain coding languages that include large folders of files that are not necessary to keep stored.
Now that the project folder is set up to be used with Github, files can now be uploaded to the repo using the relevant commands:
- `git add "file/s"` or `git add .` : this command adds specified files or all changes in the case of `git add .` to the list of "staged" changes. The staged changes are now ready to be "committed" to the repo, or, if a mistake is made, the changes can be "unstaged" and discarded. 
- `git commit -m "commit message"` : this command then "commits" the staged changes to the repo with the accompanying message associated with the changes. It is best practice and industry standard to attach a detailed and accurate message with each commit to provide accurate documentation during development.
- `git push origin master` : this command then "pushes" the changes to the repo that was set up initially, and to the branch in the command. In this case, the changes were pushed to the directory and to the `master` branch. 

### Branches, Pull Requests and Merge
In most cases developing in even a small team, changes will rarely be pushed directly to the `master` branch. Instead, changes will be pushed to another branch set up specifically to push changes to. For example, a `new style` branch may be set up to change some styling for a website. In the case of a new branch, a user can use the `git checkout -b "branchname"` to create a new branch and begin working in it. From here, a user can still `git add .`, `git commit` and `git push origin "branchname"`. At any time, a user can change working branches by using the `git checkout "branchname"` command.
	Once changes have been pushed to the new branch and you're ready to send the new code to the `master` branch, you can create a "pull request" from your repository on Github with the `compare & pull request` button.
![Create Pull Request](https://raw.githubusercontent.com/amberemeny/MERN-Workbook/master/images/newBranch.png)This creates a request to "pull" the changes down to assess compatibility with the code already present in the `master` branch. Here you can see if the code is available to be merged. You can also attach relevant information involving the changes made.
![Pull Request](https://raw.githubusercontent.com/amberemeny/MERN-Workbook/master/images/pullRequest.png)Once the pull request is made, the opportunity to merge the code will be presented. Here more information can be added to outline changes and any conflicts in code are outlined. 
![Merge Request](https://raw.githubusercontent.com/amberemeny/MERN-Workbook/master/images/mergePullRequest.png)After the merge request is made, the user will be prompted to safely delete the branch now that all changes are included in the `master` branch. It's not a requirement but it is best practice to only merge with the `master` branch once all work is completed on the new branch.
![Delete Branch](https://raw.githubusercontent.com/amberemeny/MERN-Workbook/master/images/deleteBranch.png)If at anytime the files in your local project differ from those in the repo, git may ask you to initiate a pull request. This is where any new changes in the online repo are pulled to the local machine. This can be done with the `git pull origin "branchname"` command.
If a new team member needs to download the files to also work on, this is also the command used.
### Summary
In summary, standard source control for a project will involve:
 - creating a new repo on Github
 - initializing the local project as a repo
 - adding changes to staging
 - committing those staged changes with a detailed message
 - pushing those changes to the online repo
In some cases:
 - creating a new branch for new feature/style development
 - once work has been completed on that branch, creating a pull request to merge files with the master branch
 - deleting the working branch after changes have been merged
	

## What are the most important aspects of quality software?
ISO 9126 is an international standard developed for the evaluation of software. It outlines six main qualities that contribute to quality evaluation:
 - Functionality
 - Reliability
 - Usability
 - Efficiency
 - Maintainability
 - Portability
### Functionality
Functionality is classed as the essential purpose of the software. The more functions that a product or service has, the more complicated it becomes to define it's functionality. For example, to evaluate functionality for a sales ordering system, it should be able to:
 - Record sales order product, price and quantity.
 - Calculate total price.
 - Calculate appropriate sales tax.
 - Calculate date available to ship, based on inventory.
 - Generate purchase orders when stock falls below a given threshold.
 Functionality also possesses several sub-characteristics:
  - Sustainability: refers to the appropriateness of the functions of the software for the purpose.
  - Accurateness: refers to the accuracy of the functions.
  - Interoperability: refers to the ability of a component to interact with other systems or components.
  - Compliance: refers to the compliance of the appropriate industry laws and guidelines.
  - Security: refers to the integrity of restricted access to software functions.

### Reliability
Reliability defines the capability of the software to maintain its service provision under defined conditions for defined periods of time once it is functioning and deployed. Sub-characteristics that contribute to reliability are:
  - Maturity: refers to the frequency of failure of the software.
  - Fault Tolerance: refers to the ability of software to withstand and recover from failure.
  - Recover-ability: refers to the ability to bring back a failed system to full operation, including data and network connections.

### Usability 
Usability exists with regard to functionality and refers to the ease of use for a function. The sub-characteristics associated with usability are:
 - Understand-ability: refers to the ease of which the functions can be understood.
 - Learn-ability: refers to the effort needed for various user groups to understand functionality.
 - Operability: refers to the ability of the software to be easily operated by a given user in a given environment.

### Efficiency
This characteristic is defined by the system resources used when providing the required functionality including disk space, memory and network load. The only sub-characteristics included in efficiency evaluation are time behavior and resource behavior which respectively measure response time and resource consumption.

### Maintainability 
Maintainability is evaluated by the ability to identify and fix a fault within a component. This takes into account code readability as well as modularization. Sub-categories that help define maintainability are:
 - Analyzability: refers to the ability of the system to change operating environments or adapt to new specifications.
 - Chang-ability: refers to the amount of effort required to change a system.
 - Stability: refers to the sensitivity to change of a given system that results in a negative impact.
 - Test-ability: refers to the effort needed to test a system change.

### Portability
Similar to maintainability, this characteristic is defined by how well software can adopt new environmental changes. Sub-characteristics of portability include:
 - Adaptability: refers to the ability of the system to change to new specifications or operating environments.
 - Install-ability: refers to the effort required to install the software.
 - Conformance: similar to compliance for functionality, refers to portability for software used.
 - Replace-ability: refers to how easy it is to exchange a given software component within a specified environment.

### Summary
In summary, a piece of software including, but not limited to, a web application, mobile application or OS software should meet the following standards to be categorized as high-quality software:
 - Serves a distinct purpose effectively and efficiently.
 - Developed in compliance with industry law and guidelines, standard best practice and conforming to development convention.
 - Provides security in handling user information, data integrity, intellectual property and online presence.
 - Functions free of software fault and error, if not, handled effectively.
 - In the case of environmental fault, appropriate safety and security measures are in place such as automatic backups, downtime user-facing information and security measures.
 - Has an accessible and intuitive user interface that provides smooth content delivery and experience to users of all learning levels.
 - Delivers content quickly and accurately with minimal loading times even with basic hardware specifications.
 - Developed to be modular and with DRY standards with components that are interchangeable with minimal effort.

## Outline a standard high level structure for a MERN stack application and explain the components:
MERN refers to a JavaScript Stack that is used to deploy full-stack web applications and is an acronym for the technologies used in its development: MongoDB, Express, React.js and Node.js. MERN stack components all work together to create an end-to-end framework for developers to create functional web applications with a user interface, networking, database implementation and back-end computing.
### MongoDB
MongoDB is a non-relational database where each record is defined as a document containing key-value pairs that resemble JSON objects. MongoDB is known for being flexible, easy to use and scalable. Through other technologies like the Node.js plugin Mongoose - MongoDB allows users to create their own schema. 
After installation, users can query and modify the database directly and search created collections through the Mongo shell CLI.
### Express
Express is a Node.js framework created to make it easier to write back-end code. Instead of writing code from scratch, it assists in the implementation of middle-ware and makes it easy to implement a router. 
### React.js
React is a groundbreaking framework based on JavaScript developed by Facebook. It rapidly handles changing data and allows the user to code in JavaScript to create UI elements. React has many features that makes it intuitive and encourages modular code:
 - JavaScript XML: is a HTML JavaScript extension used in react. It makes writing React components much simpler.
 - Components: essentially the building blocks of the UI. Each component can be created and designed to be called to the page individually, encouraging code re usability. 
### Node.js
Node.js provides a JavaScript environment which allows the user to run code directly on the server outside the browser. There are thousands of free packages known as "node modules" available to assist in application functionality.
### Summary
In summary, a MERN application will have:
 - A back-end developed with Node.js, incorporating Express middle-ware and various Node Module as required by the project.
 - An implemented MongoDB database with possible schema design developed with Mongoose middle-ware.
 - A Front-End developed with React.js that is responsive and renders content dynamically to the browser.

## A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?
As in a job interview, skills needed for a project on a small scale can be divided into two key areas - soft skills and technical skills. Technical skills referring to programming languages, key development concepts and network integration for example, where as soft skills refer to the abilities that are difficult to be measured due to their intangibility, like teamwork and communication skills. To go into more detail, a team developing a website should possess the following knowledge and skills.
### Soft Skills
To be effective in developing for a client, technical ability is second to soft skills. If a team cannot work and communicate with one another effectively then the resulting product would be a mess. Necessary soft skills include:
 - Effective collaboration and communication.
 - Ability to provide one another constructive feedback.
 - Able to efficiently distribute roles for development based on individual strength.
 - Constant contact and liaising with the client based on development methodologies.
 - Ability to effectively communicate with the client and decipher their needs.
### Technical Skills
The technical skills and knowledge necessary for the development of a small business website will vary with the clients needs, but in this case I will use the example of a typical business website needing a homepage, contact page, marketplace, and user management.
#### Planning
From the beginning, the team should be implementing a development methodology appropriate for the type of project and deadline. To encourage communication and feedback, implementation of the agile methodology should be encouraged. In accordance with team collaboration and role distribution, project management software such as Trello should also be implemented. Other planning knowledge and skills should include:
 - Wire framing: to create mock ups for the user interface.
 - Entity Relation Diagram (ERD) Design: to visualize the database schemas.
 - Flow Chart Design: to map the user flow of the website.

#### Development
Development knowledge and skills are going to differ in ways depending on the preference of the team and the clients needs. In this case, I'll use an example of the MERN model. Skills for development include:
 - Github: or other appropriate source control.
 - MongoDB: database implementation.
 - Express.js: network implementation.
 - React.js: front-end implementation.
 - Node.js: back-end implementation.
 - Authentication and Authorization methods: to implement the user login/logout functions and provide security for sensitive information.
 - Responsive Design: to allow users the same functionality no matter the device used.
 - Accessible Design: to assist differently-abled users in experiencing the website.
 - Testing: to ensure the website is functioning as expected and required.
#### Production
Once the website has been developed, tested and approved by the client, the team should possess knowledge on deployment methods such as Heroku, Google Firebase or Amazon AWS and how to connect a custom domain through these services. Other helpful knowledge for production would be implementing Google Analytics to help the client monitor user interaction.

## With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges? With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature:

For this example, I will refer to my personal portfolio project completed in Term 2 of the Fast Track Program. The source code for which can be found here: https://github.com/amberemeny/personal-portfolio

This project was completed at a time where knowledge, skills, and experience was very limited as I was new to a lot of concepts that were being taught. My skill repertoire at the time consisted of:
 - HTML5
 - CSS/SCSS
 - Github Source Control
 - Responsive and Accessible Design
 - Wireframing
 - Website Flow Diagrams
 - Agile Methodology/Project Board Implementation
 - Heroku/Github Pages Deployment

I had no knowledge of javascript, contact form functionality or any back-end implementation. 
Though I lacked some skills that I now find essential, I was able to create a mostly functional, responsive website, which was what was required of me for that project. 
To overcome challenges during development I had to do a lot of learning on my own accord about flexbox styling, using SCSS modularisation and mix-ins, and proper Github CLI commands. 

### Evaluation
Looking back on the completed project, I feel my knowledge was just barely effective in achieving a functional product. There were many skills that I was missing to improve my work and my productivity, but I feel that most of those skills come with time and experience, which I have more of now. The next time I tackle my personal portfolio, it will be with a clear strategy and final product in mind. For each of the skills I possessed during the project, I feel significant improvement could have been achieved with experience and knowledge: 
 - HTML5 
	  * HTML should have been implemented through React.js components to improve responsibility and load time.
	  * More semantic elements should be used to improve accessibility.
 - CSS/SCSS
	 - From the beginning, SCSS should be modularised for each element to improve readability, adaptability and changes in the future.
	 - Variables should be implemented from the beginning to make changes to color schemes quick and easy.
 - Github Source Control
	 - Regular commits should be encouraged with incredibly detailed messages to describe changes. In most instances, each change to a major element or style should be commited, just in case.
	 - Alternative branches should be implemented to play with layout and style changes.
 - Responsive and Accessible Design
	 - More appropriate breakpoints should be implemented to better reflect the most commonly used view ports.
	 - Better Alt descriptions for images to assist vision impaired users.
 - Wireframing
	 - Less styling used in wire framing.
	 - More layouts created to provide alternate options.
 - Agile Methodology/Project Board Implementation
	 - Committing to the use of Trello boards throughout development.
 - Heroku/Github Pages Deployment
	 - More advanced knowledge of CLI commands.
	 - Experience with alternatives to Heroku for deployment.
	 - Experience with connecting custom domains to deployed websites.

Other changes or improvements:
 - Implementation of React.js for front-end rendering.
	 - Heavily modularised React modules to make changes in the future easier.
 - Knowledge of contact form functionality and proper implementation.
 - Improved responsiveness using JavaScript for elements where appropriate.

## Explain control flow, using an example from the JavaScript programming language:
Control flow refers to the order statements are executed or evaluated when a program is running. JavaScript supports what are called *control flow statements* which are used to determine what section of code is run in a program. The following are examples of these statements in JavaScript:
 - Block Statements: are used to group statements, of which are surrounded by a pair of curly brackets. Block statements are commonly used with control flow statements like `if`, `for` and `while`. 
 - Conditional statements: are a set of commands that executes if a specified condition is true.
	 - `if...else`: the if statements will run if the specified condition is true. The optional `else` clause will run if the condition is false. `else if` can also be used to add additional conditions to the sequence.
```javascript
// an example of an if...else statement
let x = 3
if (x == 4) {
	statement_1;
} else if (x =< 2) {
	statement_2;
} else {
	statement_3;
}
// in this example, statement_3 will be executed because x does not equal 4, and is not less than or equal to 2.
```
 - `switch`: the switch statement allows a program to attempt to match the specified expressions value to a case label. If a match is found, it runs the associated statement. If no match is found, the program looks for the optional `default` label, otherwise, runs the next function after the switch statement.
	 - `break` statements can be included in each `case` clause to ensure the program breaks out of the `switch` loop after it's executed, otherwise the program continues to run through each `case` statement.
```javascript
// an example of a switch statement
switch (city) {
	case 'Brisbane':
		console.log('Brisbane is in Queensland.')
		break
	case 'Sydney':
		console.log('Sydney is in New South Wales.')
		break
	case 'Melbourne':
		console.log('Melbourne is in Victoria.')
		break
	default:
		console.log('Im not sure where ' + city + 'is .')
}
console.log('I hope you fouund your city.')

// If I ran the function for switch (Sydney) the console output would look like:
// Sydney is in New South Wales.
// I hope you found your city.
```
 - `while` is a loop which evaluates a condition before each loop iteration. If the result is false, the loop is finished, otherwise the loop is run again.
```javascript
// an example of a while loop.
let arr = [1, 2, 3, 4, 5]
while (arr.length > 0) {
	const elem = arr.shift() // Removes the first element and assigns it to the elem variable.
	console.log(elem) // Prints the shifted element to the console.
}
// Because the statement is essentially removing an element from the array and logging it to the console in each iteration, the console should read a list of the elements, eventually finishing when there are no more left.
```
## Explain type coercion, using examples from the JavaScript programming language:
Type coercion is the process of converting value from one type to another. There are three types of conversion:
 - to string: the String() function explicitly converts values to a string where as implicit coercion is triggered by the `+` operator, when any addition is a string:
```javascript
String(255) // "255"
255 + "" // "255"
// Examples of different data types being converted to strings.
String(true) // "true"
String(null) // "null"
String(-1) // "-1"
```
 - to boolean: the Boolean() function explicitly converts values to a boolean whereas implicit conversion happens when triggered by logical operators:
```javascript
Boolean('') // false
Boolean(0) // false
Boolean(null) // false
// Objects, functions, Arrays, Date and user-defined types are converted to true.
Boolean([]) // true
Boolean ({}) // true
Boolean(function() {}) // true
```
 - to number: the Number() function explicitly converts values to a number but implicit conversion is triggered in more cases.
	 -   comparison operators (`>`, `<`, `<=`,`>=`)
	-   bitwise operators ( `|` `&` `^` `~`)
	-   arithmetic operators (`-` `+` `*` `/` `%` ). Note, that binary`+` does not trigger numeric conversion, when any operand is a string.
	-   unary `+` operator
	-   loose equality operator `==` (incl. `!=`).  
    Note that `==` does not trigger numeric conversion when both operands are strings.
```javascript
Number(null) // 0
Number(true) // 1
Number("50") // 50
Number("hello") // NaN
```
## Explain data types, using examples from the JavaScript programming language:
Variables in JavaScript can contain any data. There are seven basic data types:
 - **Number**: represents both integer and floating point numbers. There are special numeric values such as `Infinity` and `NaN`.
	 - `Infinity`: represents mathematically infinite numbers.
	 - `NaN`: represents a computational error and stands for "not a number".
```javascript
// Examples of numbers.
let x = 12
let y = Infinity
let z = NaN
```
 - **BigInt**: in JavaScript the number type cannot represent integer values larger than 2^53^. So BigInt type was added to represent integers or arbitrary length. It's created by adding "n" to the end of an integer.
```javascript
// Example of BigInt.
let x = 1234567890123456789012345678901234567890n
```
 - **String**: a string must be surrounded by quotes. There are 3 types of quotes:
	 - Double quotes & Single quotes: There are practically no difference between double and single quotes in JavaScript.
	 - Back-ticks: are quotes that provide extended functionality by allowing us to embed variables and expressions into a string by wrapping them in `${...}`.
```javascript
// Examples of strings.
let name = "Amber"
console.log( `My name is ${name}!`)
// Output: My name is Amber!
```
 - **Boolean**: this type only has two values - true and false. It can be used to store yes/no values or be the result of a comparison.
```javascript
let likeCheese = true // Yes, I like cheese.
let isLessThan = 1 < 2 // Yes, 1 is less than 2; evaluates to true.
```
 - **Null**: the null datatype contains only the "null" value. In JavaScript, it is a special value which represents "nothing", "empty" or "value unknown". It is commonly used to fill variables with an unknown value to be changed later.

## Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language:
 - **Objects**: are a more complicated datatype used in JavaScript. They are used to store keyed collections or various data and more complex entities. Objects can be created with curly braces with optional properties consisting of key: value pairs. The key : value pairs in this case is a string referred to as the "property name" and a value that can be any data type.
```javascript
// Example of objects.
let user = {
	name: "Amber",
	age: 25,
	skills: ["Javascript", "HTML", "CSS"],
}
// Objects can then be modified using "dot notation".
user.city = "Brisbane"
// If I were to want to access information from my object:
console.log(`My name is ${user.name}. I am ${user.age} and live in ${user.city}. I love to code using ${user.skills[0]}.`
// This would output: My name is Amber. I am 25 and live in Brisbane. I love to code using Javascript.
```
 - a property can be removed using the `delete` operator:
```javascript
delete user.name
```
- aside from "dot notation", "square bracket notation" can be used to support keys with multiple words:
```javascript
user["likes cheese"] = true
console.log(user["likes cheese"])
// Output: true
```
- using functions, we can create many objects by reusing the same code:
```javascript
function createPerson(name, age, location) {
	return {
		name: name,
		age: age,
		location: location,
	}
}

let amber = createPerson("Amber", 25, "Brisbane")
let bob = createPerson("Bob", 32, "Sydney")
// To access the created objects.
console.log(bob.age)
// Bob's age - Output: 32
```
## Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language:
```javascript
// Converting arrays to strings - converts an array to a string of values seperated by a comma.
let people = ["Amber", "Sarah", "Rory"]
toString(people) // "Amber,Sarah,Rory"

// Join method joins all the array elements into a string but you can specify the separator.
let people = ["Amber", "Sarah", "Rory"]
people.join(" / ") // "Amber / Sarah / Rory"

// Pop removes the last element from an array.
let people = ["Amber", "Sarah", "Rory"]
people.pop() // people now equals ["Amber", "Sarah"]
// The popped value can be assigned this way to a variable.
person = people.pop() // person now equals "Rory"

// Push adds a new element to the end of an array.
let people = ["Amber", "Sarah", "Rory"]
people.push("Dan") // people now equals ["Amber", "Sarah", "Rory", "Dan"]
// assigning this method to a variable returns the length of the new array.
arrayLength = people.push("Dan") // arrayLength now equals 4

// Shifting is similar to popping but works with the first element instead of the last.
let people = ["Amber", "Sarah", "Rory"]
person = people.shift() // Removes "Amber" from the array and assigns it to the person variable.

// The unshift works in the same way but to add an element to the beginning of the array.
let people = ["Amber", "Sarah", "Rory"]
arrayLength = people.unshift("Dan") // arrayLength now equals 4 and the array now equals ["Dan", "Amber", "Sarah", "Rory"].

// Array elements can be accessed by their index, starting at 0.
let people = ["Amber", "Sarah", "Rory"]
people[1] = "Alex" // The array now equals ["Amber", "Alex", "Rory"]

// Splice can add elements to the array at a given index point. 
let people = ["Amber", "Sarah", "Rory"]
// The first parameter is the index at which the elements will be added, and the second is how many elements will be removed. The rest are the new elements.
people.splice(2, 0, "Alex", "Dan") // The array now equals ["Amber", "Sarah", "Alex", "Dan", "Rory"]
// This can also be used to remove an element at a specific index.
let people = ["Amber", "Sarah", "Rory"]
people.splice(1, 1) // "Sarah" has been removed from the array.

// Concat is a method that creates a new array by merging existing ones.
let people = ["Amber", "Sarah", "Rory"]
let students = ["Alex", "Dan"]
let everyone = people.concat(students) // everyone now equals ["Amber", "Sarah", "Rory", "Alex", "Dan"]

// Slice is a method that slices out a piece of an array to a new one.
let people = ["Amber", "Sarah", "Rory"]
// Passing in 2 index points will slice from the first up to the second parameter, not including it.
let girls = people.slice(0, 2) // girls now equals ["Amber", "Sarah"]
```
## Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language:
```javascript
// If you have JSON data in a Javascript file. It is likely to be assignned to a variable as a JSON object or as a string.
// Example of JSON in a .js file assigned to a variable:
let data = {
	"name" : "Amber",
	"age" : 25,
	"location" : "Brisbane"
}
// Example of JSON in string form in a .js file assigned to a variable:
let data = '{"name" : "Amber", "age" : 25, "location" : "Brisbane"}'

// A string of data is often used to pass information from a client to a server. To convert data between a string or JSON object, you can use the following methods.
let data = '{"name" : "Amber", "age" : 25, "location" : "Brisbane"}'
JSON.parse(data) // Will parse the string as an object.

let data = {
	"name" : "Amber",
	"age" : 25,
	"location" : "Brisbane"
}
JSON.stringify(data) // Will parse the data as a string.

// Once the data has been parsed as an object, its properties can be manipulated using dot and square bracket notation as covered in the Object section of the workbook.
```

## For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognize and identify functions, ranges and classes:
```javascript
// The class "Car" is initiated with a carname that will be passed in as a variable when a new object is created.
class Car {
  constructor(brand) {
    this.carname = brand;
  }

// This function will return a string that looks like "I have a (carname)".
  present() {
    return 'I have a ' + this.carname;
  }
}

// The class "Model" inherits the properties and functions of the "Car" class, so now each new object of "Model" will be passed a "brand" and "mod" variable that will be assigned as the carname and model respectively.
class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }

// This function returns the string returned by the "present" function in the "Car" class and adds a string that will look like ", it was made in (model)".
  show() {
    return this.present() + ', it was made in ' + this.model;
  }
}

// Assigns an array of car make names to the "makes" variable.
let makes = ["Ford", "Holden", "Toyota"]
//  - An array is created using the Array constructor by passing in a single number.
//  - Because the number passed in is 40, the array will be 40 elements long with an undefined value for each.
//  - An array is then created using results mapped from adding each elements position in the array to 1980. 
//  - The resulting array will be a list of years from 1980-2019, and is assigned to the models variable.
let models = Array.from(new Array(40), (x,i) => i + 1980)

// This function takes a min and max number as variables.
// A random number between 0 - 1 and multiplies it by the max-min+1, it then adds the min number to the result and rounds down.
// This is a standard function that essentially chooses a random interval between the min and max.
function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}

// For each element in models, execute the following code:
for (model of models) {

// Pass in 0 and the length of the makes array -1 (2) as the min and max to the randomIntFromInterval function. 
// Find the element in the position of the resulting number inside the makes array.
// Assign the value (string) of that element to the "make" variable.
  make = makes[randomIntFromInterval(0,makes.length-1)]

// Pass in 0 and the length of the makes array -1 (2) as the min and max to the randomIntFromInterval function. 
// Find the element in the position of the resulting number inside the modles array.
// Assign the value (number) of that element to the "model" variable.
  model = models[randomIntFromInterval(0,makes.length-1)]

// Pass in the new values of the make and model variables (should be a string and number) to a new Model class object. 
// Assign the new object to the mycar variable. 
  mycar = new Model(make, model);

// Then, excecute the function "show" in the Model class, using the newly created mycar object. 
// The result should be something like "I have a Holden, it was made in 1980".
  console.log(mycar.show())

// Repeat for each element in the models array as per the code.
}
```
