#PanX the API

 PanX uses Zoho Recruit API which allows integrating modules with third-party applications, portals or websites. You can extract data in XML or JSON format and develop new applications or integrate with your existing business applications. The API is independent of programming languages meaning you can develop applications in any programming language.

 

###You can use the API to integrate the following types of applications:

    Zoho Services
    Third-party applications

###Target Audience

    Developers
    Recruit Project Managers
    System Integrators

###Prerequisite

    You must have a valid email address to access the Zoho Recruit service.
    You must have permission to access API service (System-level security settings).
    You must have a valid AuthToken to access Zoho Recruit API (See Using Authentication Token).
    Developer environment/hosting server to integrate third-party application.
    Internet connection to communicate with Zoho Recruit API.
    

##API Methods

Method Name|Purpose
:------:|:-------:
getRecords|To retrieve all users data specified in the API request
getRecordById|To retrieve individual records by record ID
addRecords|To insert records into the required Zoho Recruit module
updateRecords|To update or modify the records in Zoho Recruit
getNoteTypes|To retrieve all note types in the user account which will be useful while adding Notes through API
getRelatedRecords|To retrieve records related to a primary module
getFields|To retrieve details of fields available in a module
getAssociatedJobOpenings|To retrieve Associated JobOpenings of a given Candidate
changeStatus|To change the candidate status with respect to the job openings in Zoho Recruit
uploadFile|To attach a file to a record
downloadFile|To download a file attached to a record
associateJobOpening|To associate candidates to job openings in Zoho Recruit
uploadPhoto|To add a photo to a contact or candidate
downloadPhoto|To download the photo of a contact or candidate
uploadDocument|To parse and upload candidate resumes from third-party applications
getModule|To retrieve all modules from Zoho Recruit account
getAssociatedCandidates|To get associated Candidates for a Job Opening
getSearchRecords|To search records by the expressions of the selected columns

##Modules & Fields

###You can use API to integrate with the following standard modules:
Standard Module|API Format
:---|:---:
Candidates|	Candidates
Clients|	Clients
Contacts|	Contacts
Job Openings|	JobOpenings
Tasks|	Tasks
Events|	Events
Calls|	Calls
Interviews|	Interviews


###Candidates
Field Name|	API Format|	Description|	Data type|	Maximum Limit
:---:|:---:|:---:|:---:|:---:
Candidate Owner	|Candidate Owner	|Select the Zoho Recruit user to whom the Candidate is assigned.|	Lookup|	-
Salutation|	Salutation|	Select the salutation from the drop-down list.	|Pick list|	-
First Name|	First Name|	Specify the first name of the candidate.	|Text box|	Alphanumeric(40)
Candidate ID|	Candidate ID	|Specify the ID of the candidate.|	Auto number|	Alphanumeric(120)
Last Name*	|Last Name*	|Specify the last name of the candidate. This field is a mandatory.	|Text box	|Alphanumeric(80)
Experience in Years|	Experience in Years|	Specify the working experience in years of the candidate.	|Double|	-
Source|Source|Select the source of the candidate i.e. from where the candidate is generated.|Pick list|	-
Highest Qualification Held	|Highest Qualification Held|Select the highest qualification held by the candidate.|Pick list|	-
Current Job Title|	Current Job Title	|Specify the current job title of the candidate	|Pick list|	-
Phone	|Phone|	Specify the phone number of the candidate.	|Text box	|Alphanumeric(30)
Mobile|	Mobile	|Specify the mobile number of the candidate.|	Text box	|Alphanumeric(30)
Fax	|Fax|	Specify the fax number of the candidate.	|Text box	|Alphanumeric(30)
Email	|Email	|Specify the email address of the candidate.	|Email|	Alphanumeric and Special characters(100)
Current Employer|	Current Employer|	Specify the current employer of the candidate.	|Text box|	Alphanumeric(100)
Website |	Website|	Specify the website of the candidate.	|URL|	Alphanumeric(120)
Candidate Status|	Candidate Status	|Select the status of the candidate from the drop-down list.	|Pick list|	-
Expected Salary	|Expected Salary	|Select the expected salary of the candidate.	|Currency|	Decimal(16)
Current Salary|	Current Salary|	Select the current salary of the candidate.	|Currency	|Decimal(16)
Email Opt-out|	Email Opt-out	|Select the checkbox to remove the candidate from your mailing list.|Checkbox|	-
Skill Set	|Skill Set	|Select the skill set of the candidate.	|Text area (long text)	|32000 characters
Street	|Street	|Specify the street address of the candidate.	|Text box|	Alphanumeric(250)
City|	City	|Specify the name of the city where the candidate lives.	|Text box|	Alphanumeric(30)
State	|State	|Specify the name of the state where the candidate lives.|	Text box|	Alphanumeric(30)
Zip Code|	Zip Code	|Specify the postal code of the candidate's address.|	Numeric|	Alphanumeric(30)
Country	|Country|	Specify the name of the candidate's country.	|Text box|	Alphanumeric(30)
Additional Info	|Additional Info	|Specify any other details about the candidate.|	Text area (long text)|	32000 characters
Twitter	|Twitter	 |Specify the twitter account details of the candidate.	|Text box |	 Alphanumeric(50)
Modified By|	Modified By	| Specify the user who modified the candidate details.	|Owner Lookup|	 -
Created By	|Created By	 |Specify the user who added the candidate details.	|Owner Lookup	| -
Resume	|Resume 	| Browse and attach the candidate resume from your system.	|Upload Text
Formatted Resume	|Formatted Resume |	 Browse and attach the candidate formatted resume from your system.	|Upload Text	 
Cover Letter |	Cover Letter	 |Browse and attach the candidate cover letter from your system.|	Upload Text	 
Others	|Others 	| Browse and attach any other details about the candidate from your system.|	Upload Text	 


###Clients
Field Name|	API Format|	Description|	Data type|	Maximum Limit
:---:|:---:|:---:|:---:|:---:
Client Name *|	Client Name *	|Specify the client name. This field is mandatory.|	Text box|	Alphanumeric(100)
Account Manager	|Account Manager	|Select the name of the user to whom the account is assigned.|	Look up	|-
Website|	Website	|Specify the URL of the company's website.|	URL|	Alphanumeric(30)
Source|	Source|	Select the source of the client i.e. from where the client is generated.|	Pick list|	-
Parent Client	|Parent Client	|Select the parent company name from the Change pop-up dialog.|	Lookup|	-
Created By|	Created By|	Specify the user who added the client details.	|Owner Lookup|	-
Modified By|	Modified By|	Specify the user who modified the client details.|	Owner Lookup|	-
Industry|	Industry|	Select the type of industry from the drop-down list.|	Pick list|	-
Client Contract	|Client Contract|	Browse and attach the client contract from your system.	|Upload Text|	-
Client Logo|	Client Logo|	Browse and attach the client logo from your system.|	Upload Text	|Number
Others	|Others|	Browse and attach any other details about the client.|	Upload Text|	Alphanumeric(30)
Contact Number	|Contact Number|	Specify phone number of the client.|	Text box|	Alphanumeric(30)
Fax	|Fax|	Specify the fax number of the client.	|Text box|	Alphanumeric(30)
Billing Address

    Street
    City
    State
    Code
    Country

	|Billing Address

    Street
    City
    State
    Code
    Country

	|Specify the billing address of the client to send the quotes, invoices, and other agreements.|	

    Street - Text box
    City - Text box
    State - Text box
    Code - Text box
    Country- Text box

|

    Alphanumeric(250)
    Alphanumeric(30)
    Alphanumeric(30)
    Alphanumeric(30)
    Alphanumeric(30)

|Shipping Address

    Street
    City
    State
    Code
    Country

	|Shipping Address

    Street
    City
    State
    Code
    Country

	|Specify the shipping address of the client to deliver the shipment.|	

    Street - Text box
    City - Text box
    State - Text box
    Code - Text box
    Country - Text box

|	

    Alphanumeric(250)
    Alphanumeric(30)
    Alphanumeric(30)
    Alphanumeric(30)
    Alphanumeric(30)

About|	About|	Specify details about the client.|	Text area (long text)|	32000 characters
 
###Contacts
Field Name|	API Format|	Description|	Data type|	Maximum Limit
:---:|:---:|:---:|:---:|:---:
Contact Owner	|Contact Owner|	Select the Zoho Recruit user to whom the contact is assigned.|	Lookup|	-
Salutation|	Salutation|	Select the Salutation of the contact, such as Mr., Ms, Mrs., or others.	|Pick list	 
First Name|	First Name|	Specify the first name of the contact.|	Text box|	Alphanumeric(40)
Last Name*|	Last Name*|	Specify the last name of the contact. This field is mandatory.|	Text box|Alphanumeric(40)
Client Name|	Client Name|	Select the client related to the contact.|	Lookup|	-
Job Title|	Job Title|	Select the job position of the contact|	Text box|	Alphanumeric(100)
Created By|	Created By|	Specify the user who added the contact details.	|Owner Lookup|	-
Source	|Source|	Select the source from which the contact is created.|	Pick list|	-
Modified By|	Modified By|	Specify the user who modified the contact details.|	Owner Lookup|	-
Department|	Department|	Specify the department of the contact.|	Text box|	Alphanumeric(30)
Twitter	|Twitter|	Specify the twitter account details of the contact.|	Text box |	Alphanumeric(50)
Email Opt Out|	Email Opt Out|	Select the checkbox to remove contacts from your mailing list|	Check box|	-
Skype Id|	Skype Id|	Specify the Skype ID of the contact. Currently, Skype ID can be in the range of 6 to 32 characters.	|Text box	|Alphanumeric(50)
Work Phone	|Work Phone	|Specify the office phone number of the contact.	|Text box|	Alphanumeric(50)
Mobile	|Mobile	|Specify the mobile number of the contact.|	Text box	|Alphanumeric(50)
Fax	|Fax|	Specify the Fax number of the contact.|	Text box|	Alphanumeric(50)
Email	|Email	|Specify the primary email address of the contact.	|Email	|Alphanumeric(100)
Mailing Address

    Street
    City
    State
    Zip
    Country

	|Mailing Address

    Street
    City
    State
    Zip
    Country

	|Specify the primary address of the contact.	|

    Street - Text box
    City - Text box
    State - Text box
    Code - Text box
    Country- Text box

|	

    Alphanumeric(250)
    Alphanumeric(30)
    Alphanumeric(30)
    Alphanumeric(30)
    Alphanumeric(30)
    
Other Address

    Street
    City
    State
    Zip
    Country

	|Other Address

    Street
    City
    State
    Zip
    Country

	|Specify the other address of the contact (if any).|	

    Street - Text box
    City - Text box
    State - Text box
    Code - Text box
    Country - Text box

|	

    Alphanumeric(250)
    Alphanumeric(30)
    Alphanumeric(30)
    Alphanumeric(30)
    Alphanumeric(30)

Is Primary Contact|	Is Primary Contact|	Select the checkbox to assign the contact as the primary contact for that organization.	|Check box|	-
Others	|Others	|Browse and attach any other details about the contact.|	Upload Text|	-


###Job Openings
Field Name|	API Format|	Description|	Data type|	Maximum Limit
:---:|:---:|:---:|:---:|:---:
Account Manager|	Account Manager|	Select the name of the user to whom the account is assigned.|	Lookup|	-
Posting Title*	|Posting Title*|	Specify name of the job opening. This field is mandatory.|	Text box|	Alphanumeric(120)
Client Name*|	Client Name*|	Select the name of the client for which the job opening has to be created. This field is mandatory.|Lookup|-
Job Opening ID|	Job Opening ID	|Specify the ID related to the job opening.|	Auto Number|	Alphanumeric(120)
Assigned Recruiter|	Assigned Recruiter|	Select the recruiter assigned to the job opening.	|Lookup|	-
Client Name	|Client Name|	Select the client related to the job opening.	|Lookup|	-
Contact Name|	Contact Name|	Select the contact related to the job opening.|	Lookup|	-
Rate|	Rate	|Specify the amount that can be expected after closing the job opening.	|Currency	|Decimal(16) 
Target Date	|Target Date	|Specify or select the expected close date. This field is mandatory.	|Date format|	-
Number of Positions	|Number of Positions	|Specify the next step of the sales process.	|Text box|	Alphanumeric(100)
Stage	|Stage	|Select the sales stage from the drop-down list. This field is mandatory.	|Pick list|	-
Probability	|Probability|	Specify the probability of closing a job opening.	|Integer|	- 
Expected Revenue|	Expected Revenue	|Calculated based on the amount and job opening stage specified.	|Currency|	Decimal(16) 
Others|	Others|	Browse and upload any other details about the job opening.	|Upload Text|	-
Job Opening Status|	Job Opening Status	|Select the status of the job opening.	|Pick list|	-
Date Opened	|Date Opened	|Specify the date in which the job opening was entered.	|Date format	|-
Industry	|Industry	|Select the type of industry from the drop-down list.	|Pick list|	- 
Job Type	|Job Type	|Select the type of job from the drop-down list.	|Pick list|	-
State	|State|	Specify the state related to the job opening. |	Text box	|Alphanumeric(120)
City	|City	|Specify the city related to the job opening.	|Text box	|Alphanumeric(120)
Work Experience	|Work Experience	|Specify the work experience required for the job opening.	|Pick List|	-
Country	Country	Specify the country related to the job opening.	Text box	Alphanumeric(120)
Modified By	|Modified By	|Specify the user who modified the job opening details.	|Owner Lookup|	-
Salary	Salary	|Specify the salary| related to the job opening.	 	 
Job Description	|Job Description	|Specify the job description.	|Text area (long text) |	32000 characters
Job Summary|	Job Summary|	Browse and upload the job summary.	|Upload Text	| -

###Tasks
Field Name|	API Format|	Description|	Data type|	Maximum Limit
:---:|:---:|:---:|:---:|:---:
Task Owner|	Task Owner	|Select the name of the user to whom the task is assigned.	|Lookup	 
Subject*	|Subject*	|Specify the name of the task. This field is mandatory.	|Text box|	Alphanumeric(50)
Due Date	|Due Date	|Specify the due date for the task|	Date	 
Contacts/Candidates	|Contacts/Candidates	|Select the related contact or candidate|	Lookup	 
Contact Name|	Job Opening/Interview/Client	|Select any other record related to the task	Lookup	|-
Status	|Status|	Specify the status of the task|	Pick List	|-
Priority	|Priority	|Select the due date.	|Date|	-
Send Notification Email|Send Notification Email|Select the check box to send notification email to the task owner|Check box	 
Remind At	Remind At	Select the check box to set reminder for the task	Check box	 
Recurring Activity	|Recurring Activity	|Select the check box to mark it as a recurring activity|	Check box|	-
Description	|Description	|Specify the details about the task	|Text area (long text)|	32000 characters
Created By|	Created By	|Specify the user who added the task details.|	Owner Lookup|	-
Modified By|	Modified By|	Specify the user who modified the task details.	|Owner Lookup	|-


###Events
Field Name|	API Format|	Description|	Data type|	Maximum Limit
:---:|:---:|:---:|:---:|:---:
Event Owner|	Event Owner	|Select the name of the user to whom the event is assigned.	|Lookup	 
Subject*|	Subject*	|Specify the name of the event. This field is mandatory.	|Text box|	Alphanumeric(50)
Start Date Time*	|Start DateTime*|Specify the date and time when the event will be started. This field is mandatory.|Date and Time	 
End Date Time*| End DateTime*|	Specify the date and time when the event will be over. This field is mandatory.	|Date and Time	
Venue|	Venue	|Enter the venue for the event	|Text	 
Contacts/Candidates	|Contacts/Candidates	|Select the related contact or candidate|	Lookup	 
Related To	|Related To	|Select any other record related to the event	|Lookup	|-
Remind At	|Remind At	|Select the check box to set reminder for the event|	Check box	 
Recurring Activity|	Recurring Activity	|Select the check box to mark it as a recurring activity	|Check box	|-
Description|	Description	|Specify the details about the event	|Text area (long text)|	32000 characters


###Calls
Field Name|	API Format|	Description|	Data type|	Maximum Limit
:---:|:---:|:---:|:---:|:---:
Subject*	|Subject*	|Specify the subject of the call. This field is mandatory.	|Text box|	Alphanumeric(50)
Call Type*|	Call Type*	|Choose whether the call is inbound or outbound.|	 	 
Call Purpose	|Call Purpose	|Select the purpose of the call.	|Pick List	 
Call From/To	|Call From/To	|Choose Contact or Candidate.	 	|-
Related To	|Related To	|Select the record to which the call is related to.|	Pick List|	-
Call Details|	Call Details	|Select whether it is a Current call, Completed call or Schedule Call.	| 	-
Call Start Time|	Call Start Time	|Automatically displays the call start date and time.	|Pick List	 
Call Duration	|Call Duration	|Specify the duration of the call.	|Integer	 
Description|	Description	|Specify the details about the task.	|Text area (long text)	|32000 characters
Billable	|Billable	|Select the check box if the call is considered for billing.|	Check box	 
Call Result|	Call Result	|Enter the call result.	|Text


###Interviews
Field Name|	API Format|	Description|	Data type|	Maximum Limit
:---:|:---:|:---:|:---:|:---:
Interview Name*	|Interview Name*|	Specify the subject of the interview. This field is mandatory.|	Text box|	Alphanumeric(120)
Candidate Name*	|Candidate Name*	|Specify the candidate name.|	Lookup|	-
Client Name	|Client Name	|Specify the client name.|	Lookup	|-
Posting Title|	Posting Title	|Specify the job opening title.	|Lookup	|-
Interviewer|	Interviewer|	Specify the user who is going to conduct the interview|	Lookup|	-
Type|	Type	|Select the type of interview.	|Pick list|	-
Interview Start Time	|Interview Start Time|	Specify the interview start date and time.|	Date Time|	- 
Interview End Time	|Interview End Time|	Specify the interview end date and time.|	Date Time|	-
Schedule Comments	|Schedule Comments	|Specify details about the interview.	|Text area (long text)	|32000 characters
Location	|Location	|Select the location of the interview.|	Text box	|Alphanumeric(120)
Interview Owner	|Interview Owner	|The interview owner is automatically displayed.	 	 
Others|	Others|	Browse and attach any other details about the interview from your system.|	Upload Text	| -
