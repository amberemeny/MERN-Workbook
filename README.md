# MERN Workbook
## Provide an overview and description of a standard source control process for a large project:
The source control is a category of software tools that provide stability and sustainability when managing source code for any development project. A version control software like Git helps keep track of every modification to the code stored for each project. The reason software like this is important is that if any code is lost, replaced or broken, the developer can review previous code, see specific changes and even roll back the whole project to an earlier saved version.

A standard source control project for a large project is usually started by creating a new, empty repository. On Github, this is done by being logged in, selecting the 

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

## A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?

## With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges?

## With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature:

## Explain control flow, using an example from the JavaScript programming language:

## Explain type coercion, using examples from the JavaScript programming language:

## Explain data types, using examples from the JavaScript programming language:

## Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language:

## Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language:

## Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language:

## For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognize and identify functions, ranges and classes:
```javascript
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return 'I have a ' + this.carname;
  }
}

class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it was made in ' + this.model;
  }
}

let makes = ["Ford", "Holden", "Toyota"]
let models = Array.from(new Array(40), (x,i) => i + 1980)

function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}

for (model of models) {

  make = makes[randomIntFromInterval(0,makes.length-1)]
  model = models[randomIntFromInterval(0,makes.length-1)]
    
  mycar = new Model(make, model);
  console.log(mycar.show())
}
```
