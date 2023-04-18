# Project for Seminars in Software and IT Engineering
Free University of Bozen-Bolzano - Faculty of Computer Science
- Dominikanerplatz 3 - piazza Domenicani, 3
- Italy - 39100, Bozen-Bolzano

- UNIBZ Roomfinder 
* Finding  Available Room to Study
* Project Documentation by:

- Danilo Fink
dfink91@gmail.com 
- Luca Pellegrini
- luca9294@gmail.com 
- Faheem Shahid
faheemshahid99@gmail.com 
- Nuzula Muscha
nuzula.muscha@gmail.com 
- Anjan Karmakar 
anjan8@gmail.com 
- Gabriele Minneci
gabriele.minneci@gmail.com 
- Heider Jeffer
hheider.jeffer@gmail.com 
- Srishti Gaihre
Srishti.kristi12@gmail.com 
* Document Status: Final Documentation
- Date(s) : December 18th, 2017
- Version : 2.0



# Theoretical Fundament of the Project “UNIBZ Roomfinder”
In this section we document which theoretical principles we applied to our project. Most of the discussed principles are described in the book “Software Engineering: Principles and Practice” by Hans Vliet. In the later section “Project Documentation and results” we will discuss how we used them and show the results.
The Software Life Cycle Revisited
In our project we decided to use agile methods to develop the application. We used agile model because it has much more flexibility with respect to traditional methods like the waterfall model. The agile process allows us to break down each of task into prioritized requirements and delivering each of task within interactive cycle. Each iteration was reviewed and assessed in a meeting every week among the project team. The feedback and comment gained from the meeting are used to determine the next step in project development. 

Our way of working is quite near to the Scrum Model. In each meeting we had a working version of the program with the requirements, chosen in the last meeting, implemented. 
In the meeting we commented the work of others and prioritized the requirements to be implemented in the next sprint. We used Trello in order to manage the Backlog Board and have an updated view of the status of the tasks. 
People Management and Team Organization
After the first weeks and meetings, we tried to fit our coordination and organization into some of the discussed practices from the book. To find out how to manage the different people in our team we first looked into Mintzberg’s Coordination Mechanisms. Our groups organization was carried out quite natural, but we still tried to fit it to one team organisation techniques discussed in the book.
Software Quality
During our initial discussions, we inherently agreed upon five quality factors that our project must satisfy. The factors being:
●	Correctness
●	Reliability
●	Efficiency
●	Usability 
●	Portability
With Correctness, we wanted to ensure that our application satisfies its specifications and fulfills the basic objectives of the user which is to find available rooms in the university.

With Reliability, we wanted to ensure that our application is reliable whereby it performs its intended function as and when needed with a high degree of precision.

With Efficiency, we wanted to ensure that the computing resources and code required to perform the basic function must not be overwhelming for the device to handle, and it should return the results within a few seconds.

With Usability, we wanted to ensure that our application was easy to use, and the effort required to learn, operate and prepare the input, is minimal.  

And with Portability, we wanted to ensure that our application can run on devices with different hardware/software configuration environment and resources. That our device should be cross-platform.

To maintain the software quality, we depend on a simple version of the Personal Software Process technique.


## Cost Estimation
Software development costs are usually difficult to estimate reliably in the early phases of its production. And even though there are a number of cost estimation formulas, we know that blind application of any of the formulae from existing models will not yield a good estimate. 

In our case we have a project with angular which is a relatively recent technology, therefore it is hard to find extensive accounts reliable data with a significant sample size. Consequently, we have chosen to determine the cost of our project by a combination of expert-based technique and simplified cocomo model.


## Estimation Procedure
First we determine the estimate of lines of code required in terms of Object points, and make a schedule of the tentative time required to complete the project based on inputs provided by the team of expert-developers. We can then calculate the estimate for the man-months required, and thereby derive the price for the entire project based on the man-month price-value evaluation. Later we compare it with the actual time take, the KLOC, and the costs involved to verify and consolidate our estimates.

The initial and final estimation procedures and their comparison are discussed later. 


## Project Planning and Control
To get a better viewpoint at our project we analyzed its characteristics (certainties of product, process and resources) to be able to match it with one of the four archetypal control situations (Realization, Allocation, Design, Experimental). After this we prepared a Work Breakdown Structure to find possible activities during our project. We estimated the costs of the different activities and assigned prerequisites to each of them. We also made a Gantt Chart, but we didn’t find it fitting our development style after seeing how we were switching between activities.

## Requirement Engineering
We discussed the functional and nonfunctional requirements especially in the earlier iterations of the project. 
We made at first general requirements, after having created the first scratch of the User Interface we improved them as they are now.


We focused more on the product functionalities, defining mainly the requirements needed for the project development and the most necessary for letting it work. 
Since we have decided the requirements by ourselves, they are general so that we had more options for the design and implementation phases. 
We manually verified and validated the requirements during the weekly meetings.

## Modelling
To have clear understanding about our requirement, we have developed modeling diagram such as Entity Relation Diagram, Sequence Diagram, Data Flow Diagram and Finite State Machine. The diagrams explain how the system should behave in relation to other functions and/or classes.

These modelling techniques are often used in Software Process Management, Requirements Engineering and Design Engineering, where models can vary from basic sketch of system to classified behaviour of systems. Most common notations that are used in making models are Box and Line sketches, and UML diagrams. These Box and Line sketches, and UML diagrams are helpful in communication between the user and the requirements engineer and between the requirements engineer and the developer.

In Unified Modeling Language(UML) boxes may denote a part of system or a single component of system, and Lines may denote the relation between the components. By using UML notations we also get to know the flow the system and communication between the different parts of the systems. Essentially, modelling techniques provide a design framework to the developers to enable them to understand and deconstruct major systems as different subsystems. 





## Software Architecture
In software architecture, we design the architecture of how the application will retrieve information about room and its availabilities between client and server side.

We use our proxy server to get the list of all the lectures (and the lecture rooms) of a particular day from UNIBZ API, while we get the information about the list of all the rooms, from In-Memory API. Our services takes the data from both the APIs and compute the free rooms. The filters are applied to the obtained data and displayed in the User Interface. 

The architecture and the description is described in detail in the later section.

## Software Design
We have used the Agile approach also for the software design. We have designed our product through different levels of abstraction: at the beginning we focused on the core components and the general modules of the software, without designing all the specific objects and relations inside them.In the successive iterations we have modelled the different modules we were using in more details. 

The design of the system is dependent by the structure of the framework we have used. The modularity we have created has been useful for assigning the implementation tasks in the team, but the more we advanced in the implementation, the more a change could affect the functionalities of other modules. As a consequence more coupling is added, we will see examples in the documentation and results section.

We have tried to put as much information hiding as we could in the various components, so that the program results with less coupling and more reusability. The angular framework gave us guidelines to relate some type of objects instead of others, for instance the services have complete access to the specific components they support, but not to the others.

Based on the fact that our product is not big, we didn’t focus too much on its complexity. We have tried to make a good design following the main best practices.





Software Testing
As already said, our project is based on the Angular framework. Angular provides essentially two main tools for testing Karma and Jasmine. 

We used Karma to test the services.
Karma is a JavaScript command line tool that can be used to spawn a web server which loads your application's source code and executes your tests. You can configure Karma to run against a number of browsers, which is useful for being confident that your application works on all browsers you need to support. Karma is executed on the command line and will display the results of your tests on the command line once they have run in the browser.
Karma is a NodeJS application, and should be installed through npm/yarn. 

We used Jasmine to test the angular components. 
Jasmine is a behavior driven development framework for JavaScript that has become the most popular choice for testing Angular applications. Jasmine provides functions to help with structuring your tests and also making assertions. As your tests grow, keeping them well structured and documented is vital, and Jasmine helps achieve this.

## Software Maintenance
For the software maintenance part we did not have plan yet, because the system is not accessible to all unibz students yet. Consequently, we are not able to measure the performance and accessibility of the system. Thus, further maintenance was thus not taken into consideration. 

However, maintenance of the system is absolutely essential once the application comes into widespread operation, in order to make sure the system functions and apis are working as expected.Furthermore, the user feedback may give us valuable insight on the working of the system, and their feedback can help evolve the system sustainably over time.

## Software Tools
At the beginning we have chosen the tools to use for the different task according to how they fit with them and our previous experience. The mandatory tools for using the specific technology we have chosen had to be learnt by the entire team: we spent a significant amount of time in the first phase in learning and getting used to our technology stack. 



For the specific tasks, each of us chose the best tools we already knew. We shared previous personal experiences with the other team members for common problems encountered in our learning curve. Since the project is small, the main tools are used to support the development phases, yet we have also used some tools for the team cooperation.

## User Interface Design
After the requirements were defined, we started with specifying the User Interface in details. We did brainstorming and came up with a mockup UI using Paint as our preliminary User Interface, which is then refined multiple times throughout the project implementation when we find any possible improvements. 

For specifying the user actions, we used User Action Notation technique which is described in this section in details. For evaluation of the user interface, we used the Heuristics evaluation techniques where we used the principles proposed by Nielsen, as given in the book. Here are some of the principles we used to evaluate the usability of our user interface.


1.	Match between system and the real world: We checked if our UI is understandable by our user.

2.	User control and freedom: Our project provides the user with the freedom to user to have their own filters.

3.	Consistency and standards: We evaluated the consistency of our project and assured that our project follows the standards. For example, we use the asterisk to specify the field is required.

4.	Recognition rather than recall: We evaluated the project and assured that the user does not have to remember so we provide the user with drop down menus.

5.	Aesthetic and minimalist design: We used the aesthetic and minimalist design. We evaluated and assured that our project’s UI does not overload user with unnecessary information.



## Software Reusability
We plan to use existing API from university that sends information such as: Building, Room, Time and Date into our application. We also use angular.io as our framework to build our application. We see that this API is compatible with the angular framework and it serves many useful data that can be used in our application. Therefore, we are reusing the existing unibz API for university lectures. Other than that the angular framework allows us to reuse some of the predefined features.



# Project Documentation and results
In this section we want to show and discuss the results we achieved in our project.
## The Software Life Cycle Revisited
At beginning of the project, we had to choose which software methodology best suited our project needs. Do we want to be AGILE or do we want to follow a more traditional approach? 
Being a young team and foreseeing high probabilities to have frequent changes in the requirements, we opted for an AGILE approach.

Being AGILE, we did not spend a lot of time doing a very detailed requirements analysis and elicitation at the beginning, but we selected only some basic features to implement for the first sprint, being aware that the requirements will change and will be more detailed going on with the project. 

Being the team composed of 8 members, we also decided to work in pair-programming.
Being not a real project, we did not have users/clients that gave us a feedback: at each meeting we had to simulate the users giving opinion/feedback about the work done by the other pairs. 

Have we been really AGILE? For sure. At each meeting, we had a working improved version of the application and each pair said what it has been done and the problems encountered. 
In the second part of the meeting, we discussed about the tasks for next iteration. 
## People Management and Team Organization
To be able to find the right mechanisms and organisations, our team first needed to get to know each other a bit, to find out which way we wanted to go.

## Mintzberg’s Coordination Mechanism: Divisionalized Form
Looking at the different coordination mechanisms we found that a sort of divisionalized form was the one we were actually already carrying out. The tasks that were assigned could be pursued in total autonomy and in weekly meetings the group checked if the goals have been reached in a sufficient manner. For us this was a good way of working, since all of us came from different backgrounds and had different experiences. 
Once the requirements and the architecture was set, we tried to split the group into subgroups with different responsibilities. We had people being responsible for the backend, a second group was responsible for the frontend and design and the third subgroup took to testing. The weekly meetings have been held to check whether a group run into problems and what the next steps would be. These technique allowed us to verify and validate activities, to discover errors or assess the quality of the code.



## Team Organisation: Agile Team
As stated before we assigned most tasks of the project to mainly 3 teams carrying out a specified role. In a normal case we had 2 people working on each team, and 2 people being jumpers meaning they would help where needed. But also each team had the possibility to ask for help from other teams, resulting in a reassignment of a person of one team to another. We clearly didn’t want to propose any hierarchical organisation because we wanted everyone to feel on the same level and have equal opportunities at the beginning of the project. Throughout the project another one of our goals was always to find the right people for the tasks that were due.

## Software Quality
The quality factors we included in our project, namely: Correctness, Reliability, Efficiency, Usability, and Portability were validated at every incremental stage of the project by checking out how many requirements were implemented at the end of the every sprint and whether or not they support the quality factors. In cases, where the quality factors were not supported, the task was set for the new sprint and the quality demands were met. 

The three steps in the process:
> Data Collection > Discussion and Analysis > Constant Improvement 


## Cost Estimation
As discussed earlier, most major algorithmic cost-estimation models are based on extensive data about past projects. But since we lack enough quantitative data about past projects which use the same technology stack as we do, we cannot possibly rely solely on a predefined model. 

Therefore, we have chosen to determine the cost for our project based on a combination of expert-based techniques and simplified cocomo.
EARLY STAGE: Early Effort and Cost Estimation

## Cost Determination 
First we determine the estimate of lines of code required in terms of Object points, and make a schedule of the tentative time required to complete the project based on inputs provided by the team of expert-developers. We can then calculate the estimate for the man-months required, and thereby derive the price for the entire project based on the man-month price-value evaluation.


## KLOC Estimation based on Object modules














