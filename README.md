# EmailSMS
Send text messages for free from ServiceNow
Role(s)
N/A OOB Notification Roles and User Table Roles

Configure SMS Email
Navigate to the user records you wish to send SMS to.

User Administration -> Users | Filter Target User
In the List View Configure Personalized List
Add Mobile Phone, Mobile Provider and Cell Email to your list
Make sure that the user has their mobile number provided
Assign the mobile carrier in the mobile provider reference
The Cell Email should auto populate
Navigate to System Notification -> Email -> Notifications
Create a notification rule where it emails sys_users.u_cell_email
Example
The customer would like to send a text message to the group manager when a P1 incident has been reported.

We first need start by creating an email notification rule that is assigned to the incident table. We only want to notify the manager via text messages 1 time so we utilize the following configurations:


Then we define the who will receive as Assignment Group.Manager.Cell Email

This will allow us to send a text message to the manager of the assignment group for the P1 incidents.
