# SpringOne-Camunda-Coding-Challenge
A fun way to learn Camunda and win a small price. The coding challenge is designed for the SpringOne Conference. Results can be hand in from the **1st of September till the 08th of September 2021**. 

##How to win? 
- Fork this repo
- Do the tasks.
- Send us a link to your fork and your address in order to ship a price to community@camunda.com with the subject: "SpringOne Coding Challenge"

##Prerequirements 
- Make sure you have Java installed and that you use a version below 15. 
- Install the [Camunda Modeler](https://camunda.com/download/modeler/) on your machine
- Fork the project and open it in your IDE

:tada: You are ready to hack!

##The challenge

### challenge 1: Get the right order of the process
Inspect the project:
![project structure](/img/project.png)

Navigate to src/main/resources and open the process.bpmn in the Camunda Modeler! 

You will see a process similar to this one: 

![project structure](/img/process-without-tasks.png)

Below the connected process with sequence flows, gateways and events you see tasks that are unconnected. The tasks form the story of the movie Pulp Fiction. Place them in the right chronological order on the sequence flow.

### challenge 2: Correct the variables

In order to get the right story plot you have to change some of the variables in the task: 

**Script Task "Royal and Cheese conversation":** 
Make sure that the the variable "lastTravel" is set to "Europe". To do so select the Script Task and open in the Camunda Modeler on the right hand site the Property panel and inspect the inline Script

**Service Task: "Prepare To Go Out With Mia"**: 
This Service task is implemented as a Delegate. Go into your IDE and look in the path: src/main/java/camunda.example.workflow for the "PrepareToGoOutDelegate". Change inside the Delegate the variable "drug" to "heroin". 

### Run the application (process)
If you want to try out your solution and run it you can start the the application class in the project. Once the application has started type in your browser: http://localhost:8080/camunda/app/welcome/default/#!/login . Log in with the credentials: username: demo, password: demo .

Choose the Tasklist application:
![project structure](/img/applications.png)

Start the process from there:
![project structure](/img/startProcess.png)

Observe your Terminal in your IDE and see what will be printed.

In the web applications you can use the house symbole in the right corner to switch between the application: 
![project structure](/img/house.png)

Go to Cockpit. In order to observer your process instances select running instances. 
![cockpit](/img/cockpit.png)

(Note: If your process instance has ended already you won't see it anymore. A running process instance is marked with a blue token)
![user task](/img/usertask.png)

If your process instance stands on a User Task. Naviagte back to Tasklist. You should see here an available task. Claim the task and complete it. 







