# Angular Lesson with Stackblitz
This lesson is to learn more about Angular, TypeScript-based open-source web application framework which generates part of the website into components for the Front End & Back End.
Below are the steps to set up Angular locally; however, for this lesson we are going to use Stackblitz. Stackblitz will allow for us to work with Angular and look at other frameworks without having to download anything.

# Stackblitz
Visit [https://stackblitz.com/] to check out what can be created! This will link to your GitHub account to save progress on your projects so it is recommended to have a GitHub account. 

# Getting started with Angular locally
1. First install Angular with npm install -g @angular/cli

2. Create a new project with ng new “name”. Example, ng new ToDoList

3. To run and serve the application locally, ng serve 

4. Check out localhost:4200

# Let's Get Started!
1. When you get to Stackblitz look in the far left corner and click on Angular. This will direct you to a new Angular Project 

Lets take about what we see!
1. On the left hand side we have the files for our project, the middle is the text editor, and the far right is the ouput console
2. All of our code is in the source folder and we have a angular.json file 
3. Inside of the source folder we have the app folder which will hold all of our components. This folder houses:
  1. app.component.css - This is the css file for the app and Angular allows for other style sheets such as Sass
  2. app.component.html - This is the html for the app
	<app-list></app-list>
  3. app.component.ts - The typescript file for the components
  4. app.module.ts - This will load in all of the Angular components
  5. hello.component.ts - This has the hello page
  6. index.html - We need to set the app to travel through this page
	<app-root></app-root>
  7. main.ts - The main typescript
  8. polyfills.ts - This are needed for Angular and we are not going to adjust them
  9. styles.css - The main styles for the app
          

2. Now it is time to add components and model! Everything in Angular is broken down into components. So for us at the moment we are going to to and program 1 componentand  1 model. To add a component in Stackblitz, right click on the app folder and you should see Angular Generator. Click on that and you should be able to add a component along with a few other things. Name the component list.

Let's take a look at what these things are!
1. Component This will give us all of the files we need to add a component
2. Service  A class with a specific purpose of sharing data, can be used to send data between the back end and front end
3. Directive : A function that executes whenever the Angular compiler finds it in the DOM (Direct Object Model)
4. Module : This is used to group components, directives, pipes and services that are related
5. Pipe : Used to transfer values in another template
6. Guard : Code that is executed before the route is loaded
7. Interface : Abstract type that does not contain any class code
8. Class : Can be used to bind muiltple classes together, in Angular, can be useful to bind CSS classes to HTML
9. Enum : A set of named constants 
	
    After the list component is created, right click on the app folder and add a new folder called model. Add a file called task.model.ts in this folder
   
3. Let's add the model code first. This is a representation for every item that we are adding to the list 
```export class Task {
  public title: string;
  public description: string;
}
```

4. After the model is done, let's look at the code that has been given to us for the component
      1. list.component.css - Has all of the css for the file
    ```  h1 {
  		text-align: center;
	}

	.task {
 		 background-color: #dbc5f7;
	}
	```
  2. list.component.html
  	```	<h1>
			What do we have to do today?
		</h1>
		<div>
			<button (click)="addTask()" style="background-color: #bfe5f6">Add Task</button>
				<!--This will add the next task-->
		</div>

		<div class="task" *ngFor="let task of taskList; let i = index">
				<!--Angular for loop to display all of the tasks; could implement database -->
		<div>
			<span class="title">Task number:</span> {{i +1}}
				<!-- Giving the task an ID-->

			<span class="remove">
  			    <button (click)='removeTask(i)'> X</button> <!--Button to remove the task-->
    			</span>
		</div>
		<div>
			<span class="title"> Title:</span>
				<!--Each task has a title an description -->
			<input [(ngModel)]="task.title" type="text">
 		 </div>
		<div>
			<span class="title"> Description:</span>
			<input [(ngModel)]="task.description" type="text">
  		</div>
		</div>
	
	
3. list.component.ts
   	```	import { Component, OnInit } from "@angular/core";
		import { Task } from "../model/task.model";

		@Component({
		  selector: "app-list",
		  templateUrl: "./list.component.html",
		  styleUrls: ["./list.component.css"]
		})
		export class ListComponent implements OnInit {
		  constructor() {}

		  public taskList: Task[] = [];

		  ngOnInit() {}

		  addTask() {
		    //Add task to the stack
		    this.taskList.push(new Task());
		  }

		  removeTask(index: number) {
		    //Remove with splice
		    if (index > -1) {
		      this.taskList.splice(index, 1);
		    }
		  }
		}
	```

5. That is it! We should have a working Angular application in Stackblitz! If things do not work out, the code in this repo can be downloaded locally.

Here are additionally resources :
        Angular Tutorial - [https://github.com/8Tesla8/to-do-list]
        Medium Angular Tutorial - [https://medium.com/weekly-webtips/simple-to-do-list-in-angular-247cdad31280]
        Angular To Do List with Material - [https://stackblitz.com/edit/angular-todolist-materialui]
