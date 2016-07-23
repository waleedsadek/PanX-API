#PanX the API

 PanX uses Zoho Recruit API for integrating modules with third-party applications, portals or websites. You can extract data in XML or JSON format and develop new applications or integrate with your existing business applications. Zoho Recruit API is independent of programming languages, you can develop applications in any programming language (Java, .Net, C, C++, PHP, etc.).

 

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

|Method Name|   	  |Purpose|
|:-----------:| |:-----------------------------------------------------------------------------------------:|
|getRecords|	          |To retrieve all users data specified in the API request|
|getRecordById|   	  |To retrieve individual records by record ID|
|addRecords|    	  |To insert records into the required Zoho Recruit module|
|updateRecords| 	  |To update or modify the records in Zoho Recruit|
|getNoteTypes|         	  |To retrieve all note types in the user account which will be useful while adding Notes through API|
|getRelatedRecords|	  |To retrieve records related to a primary module|
|getFields|		  |To retrieve details of fields available in a module|
|getAssociatedJobOpenings||To retrieve Associated JobOpenings of a given Candidate|
|changeStatus|		  |To change the candidate status with respect to the job openings in Zoho Recruit|
|uploadFile|		  |To attach a file to a record|
|downloadFile|		  |To download a file attached to a record|
|associateJobOpening|     |To associate candidates to job openings in Zoho Recruit|
|uploadPhoto|	          |To add a photo to a contact or candidate|
|downloadPhoto|	          |To download the photo of a contact or candidate|
|uploadDocument||To parse and upload candidate resumes from third-party applications|
|getModule|               |To retrieve all modules from Zoho Recruit account|
|getAssociatedCandidates| |To get associated Candidates for a Job Opening|
|getSearchRecords||To search records by the expressions of the selected columns|

