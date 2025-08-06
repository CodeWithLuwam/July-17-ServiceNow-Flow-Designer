# ServiceNow-Flow-Designer #

First activity works with Action
----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------
Workflow Studio Homescreen
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Workflow%20Studio%20Homescreen.png?raw=true)
We'll click on the New button, and then on the drop down, Flow.
- We'll give it a name that represents what the task is and click Build Flow to continue
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Name%20the%20Flow%20.png?raw=true)
- Here, we start off by creating our Trigger
  - We want a ticket to go out when a User submits an incident
  - We are working with a record, since the task is when a record is created
 ![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Workflow%20Studio%20Record%20Created.png?raw=true)
- And we will select the Incident table since its hwe an Incident gets created and press done for now.
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Select%20Incident%20Table.png?raw=true)
- So, we have our Trigger, now we need an Action and we'll press the + sign under Actions.
  - We have the option for 'Action', 'Flow Logic' or 'Subflow, but we will pick Action
    ![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Options%20under%20Actions.png?raw=true)
- The Action we choose will be to "Send Email" under ServiceNow Core
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Action%20is%20to%20Send%20Email.png?raw=true)
- For *To, we can select from our data pill to find the path which is:
    Trigger - Record Created > Incident Record > Caller > Email
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Trigger,%20Incident%20Record,%20Caller,%20Email.png?raw=true)
- We can also do the same dynamic path through the data pill for Subject and Body of the email
----------------------------------------------------------------------------------------------------
To test, we can submit an incident in the incident table and then check the Outbox.

For now, we will use the Test option in Workflow Studio.
- Our condition is a incident record has to be created. Right now we have the option to select an incident record. But if we select it, that's not going to trigger our flow. So we have the option to press that + plus button and create a new record from the testing section.
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Test%20flow%20in%20Workflow%20Studio.png?raw=true)
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Creating%20an%20Incident%20to%20test%20Workflow.png?raw=true)
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Run%20Test%20on%20Test%20Flow.png?raw=true) <br>
We'll click View the details:
The email sent shows the Trigger State is Complete, it was able to pull the user's email, the incident 
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Test%20Run%20Results.png?raw=true)
----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------
Second activity works with Flow Logic
----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Flow%20Logic.png?raw=true) <br>
Creating Conditions <br>
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Flow%20Logic%20If%20Statement.png?raw=true) <br>
We'll give our condition a name and we can drag and drop or dot walk <br>
![](https://github.com/CodeWithLuwam/ServiceNow-Flow-Designer/blob/main/Images/Condition%20Path.png?raw=true)
