# ExperimentalRobotics-Assignment1
# 1)Intoduction to the Assignment:
The assignment is done for the experimental robotic labarotary.the assignment done in the Ros platform.In this assignment an architecture is created to build an environmental ma using ontology.For using ontoogy concept in Ros,an special pakage whic is called as **Armor** is been used.Also **Smach** package is also been used to visualize the change in state when the robot moving around the environment.

# 2)Map of the Environment:
<img width="212" alt="image" src="https://user-images.githubusercontent.com/80621864/207283458-d16bc105-cf9e-42a7-8b10-9c0efe5fbf26.png">
The above figure represents the map of the environment which consists of four rooms and three corridors.the working principle of the robot relates to a surveillance policy.the robot should mainly stays in corridor and when there is an ugency.it should visit the neary rooms.

# 3)Working:
![Exprob1](https://user-images.githubusercontent.com/80621864/207284327-4535668a-4429-44a3-9208-8ddcd7c20b84.gif)
The above shown video explains the overall working of this assignment,where the robot initially starts from location **E** and when the Map is loaed,the robot reaches any one of the Corridor **C1** or **C2** then it stays there until an urgency arrives.if there is an urgency the robot visits the nearby room.if there are two or more urgency rooms the priority is given based upon the timestamp property.the **Armor** package is used to query to know the robot position,timestamp.if the battery is low the robot should reach location **E** and charge until battery is full.

## 4)The Software Architecture:
![fsm drawio](https://user-images.githubusercontent.com/80621864/207285992-d146080c-bc5b-45cd-af50-1efe4086151c.png)
This figure represents the connection between all he nodes to the **Finite_state_machine** node.
where the robot-state node sends the battery level to the Finite_state_machine and sets pose is sent to controller,get pose is sent to planner which are the two ation servers used to plan and cntrol he movement of the robot if here is an external stimilus like battery low arrives,the planner cancels the goals.Armor node helps to query and using the reult from armor the property of robot setup such as "isIn" roperty. 

## 5)Installation:
To run the assignment and to visualize the working of statemachine,follow the steps mentioned below.
```
$ cd ros_ws/src/
$ git clone "git@github.com:Aathee1103/ExperimentalRobotics-Assignment1-.git"
$ build usingcatkin_make
```


