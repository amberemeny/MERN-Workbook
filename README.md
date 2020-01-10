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
