Summary:

A ready-to-use UiPath workflow for Outlook Automation that can be integrated easily with any project across different customers that too without any modification.


What it is?

Read email and download attachments is one of the most common functionality that we come across in almost every RPA implementation.

Email with a specific subject is set as a trigger point to start the process execution. BOT reads only those emails from Outlook Inbox whose subject matches with the search criteria mentioned in config file.

BOT reads one email at a time and mark the status as read. It does not change the status of the other emails present in Outlook Inbox. 

If email has one or more attachment, it creates the folder Data\Input inside project repository and save the attachment(s) in it

Successfully tested the execution for different customers. It works very well without any change in code. It can be run standalone or can be integrated with any project.


Project repository details:

1. /Data/Config.xlsx
2. Read Email.xaml
3 .project.json


How to use Read Email By Subject Plug & Play workflow?

Filename: Read Email.xaml

(A) Pre-requisite: 

Download the complete project repository

(B) Update Config.xlsx: 

Optional: Update the value (e.g. ABCD@Company.com) against the Mail Account in “Data\Config.xlsx”. This field is useful if there are more than one email account configured in Outlook. If it is left blank, BOT will monitor primary mailbox by default. 

Optional: Update the value (e.g. ‘Inbox’ or ‘Inbox\UiPath’) against the Mail Folder in “Data\Config.xlsx”. If it is left blank, emails will be read from the Inbox folder by default. 

Enter the search criteria (text) for email subject. BOT is configured to read the email by searching the keyword in subject of the email. 

Note: Config should have the REFramework structure

(C) Invoke: Integration with existing project 

Use Invoke Workflow activity in your project sequence/workflow 

Click import arguments 

Optional: Pass Config (Data Dictionary) variable to the input argument in_Config, if you are using ReFramework

(D) Run: Standalone execution
