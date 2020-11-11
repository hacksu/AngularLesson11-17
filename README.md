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
          

2. Now it is time to add components! Everything in Angular is broken down into components. So for us at the moment we are going to to and program 1 componentand  1 model. To add a component in Stackblitz, right click on the app folder and you should see Angular Generator. Click on that and you should be able to add a component along with a few other things. Name the component list.
      Let's take a look at what these things are!
      
        1. Component : This will give us all of the files we need to add a component
        
        2. Service :  A class with a specific purpose of sharing data, can be used to send data between the back end and front end
        
        3. Directive : A function that executes whenever the Angular compiler finds it in the DOM (Direct Object Model)
        
        4. Module : This is used to group components, directives, pipes and services that are related
        
        5. Pipe : Used to transfer values in another template 
        
        6. Guard : Code that is executed before the route is loaded
        
        7. Interface : Abstract type that does not contain any class code
        
        8. Class : Can be used to bind muiltple classes together, in Angular, can be useful to bind CSS classes to HTML
        
        9. Enum : A set of named constants 
   
3. Now that we have created the list component we  need to look at the files that have been generated for us
        1. 
