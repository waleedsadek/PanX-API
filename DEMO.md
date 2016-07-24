###Permission:
"Recruiter-Admin" role only will able to access all Zoho APIs.

###To generate Ticket ID (ticket): 

 Give the username and password of "Recruiter-Admin" role

 
<form method="POST" action="https://accounts.zoho.com/login" target="_self">
<input type="hidden" name="LOGIN_ID" value="[ZOHO ID or Email ID]">
<input type="hidden" name="PASSWORD" value="[Password for ZOHO ID]">
<input type="hidden" name="FROM_AGENT" value="true">
<input type="hidden" name="servicename" value="zohopeople">
<input type="submit" value="Get Ticket ID" class="divbutton" name="submit">
</form>

###RESPONSE:
# #Thu Apr 01 20:29:06 PDT 2010
GETUSERNAME=null
WARNING=null
PASS_EXPIRY=-1
TICKET=5767ef44382712202e432d57da576b34
RESULT=TRUE

 
Get the TICKET from the RESPONSE above.

###To generate API Key (apikey):
Login to http://zapi.zoho.com to get your API Key, which you need to pass with every API request

###To access the below available API's:
Request URL to getRecords:

**XML:**http://recruit.zoho.com/ats/private/xml/~~**Module**~~/getRecords?apikey=API Key&ticket=Ticket
**JSON:**http://recruit.zoho.com/ats/private/json/~~**Module**~~/getRecords?apikey=API Key&ticket=Ticket

Replace Module with any one of this *JobOpenings*, *Candidates*, *Clients*, *ClientContacts*, *Users* 

Request Parameters:
Parameter|Data Type|Description
:---:|:---:|:---:
ticket*|String|Encrypted alphanumeric string to authenticate your Zoho credentials. You can use the same ticket for 7 days. After 7th day, you must generate a new ticket.
apikey*|String|API key to access your Zoho CRM account.
fromIndex|Integer|Default value - 1.
toIndex|Integer|Default value - 20 Maximum value - 200.
sortColumnString|String|If you use the sortColumnString parameter, by default data is sorted in ascending order.
sortOrderString|String
searchCondition|String|(Created By|=|username)

*** - Mandatory parameter**
Default value - asc
if you want to sort in descending order, then you have to pass sortOrderString=desc.

**Regular Expressions**
You can specify the following expressions in API request:
is OR =

isn't OR <>

contains(*srcString*)

starts with(srcString*)

ends with(*srcString)

doesn't contain

< OR is before

> OR is after

<=

=>

###Request URL to getRecordById:
**XML:**http://recruit.zoho.com/ats/private/xml/~~**Module**~~/getRecordById?apikey=API Key&ticket=Ticket
**JSON:**http://recruit.zoho.com/ats/private/json/~~**Module**~~/getRecordById?apikey=API Key&ticket=Ticket

Replace Module with any one of this **JobOpenings**, **Candidates**, **Clients**, **ClientContacts**, **Users**

Request Parameters:
Parameter|Data Type|Description
:---:|:---:|:---:
ticket*|String|-
apikey*|String|-
id|String|Specify unique ID of the record.

*** - Mandatory parameter**

###Request URL to addRecords:

**XML:**http://recruit.zoho.com/ats/private/xml/~~**Module**~~/addRecords?apikey=API Key&ticket=Ticket
**JSON:**http://recruit.zoho.com/ats/private/json/~~**Module**~~/addRecords?apikey=API Key&ticket=Ticket

Replace Module with any one of this **JobOpenings**, **Candidates**, **Clients**, **ClientContacts**, **Users** 

Request Parameters:
Parameter|Data Type|Description
:---:|:---:|:---:
ticket*|String|-
apikey*|String|Specify API key of your Zoho CRM account.
xmlData*|XML|This is an XML string and the format should be same as of getRecords in XML format of fetched records.
duplicateCheck|Integer|Set value as "1" to check the duplicate records and throw an error response or "2" to check the duplicate records, if exists, update the same.

*** - Mandatory parameter**

Duplicate Check Fields:
Module Name|Duplicate Check Field
:---:|:---:
JobOpenings|Posting title
Candidates|Email ID
Clients|Clients
ClientContacts|Email ID

###Examples:

Insert records into Zoho Recruit from third-party applications

**URL Format:** http://recruit.zoho.com/crm/private/xml/JobOpenings/addRecords?apikey=APIKEY&ticket=TICKET&xmlData=XMLDATA

###XMLDATA JobOpening example:
<JobOpenings>
<row no="1">
<FL val="Posting title">Java Developer</FL>
<FL val="Client">ZOHO</FL>
<FL val="Assigned recruiter">0001</FL>
<FL val="Client manager">0001</FL>
<FL val="Job opening status">In-progress</FL>
<FL val="Number of positions">5</FL>
<FL val="Country">INDIA</FL>
<FL val="Roles and responsibilities">Develop web service with proper data model</FL>
<FL val="Attach doc">TVlTUUwgMTkyLjE2OC4xNS40NCAxOTIuMTY4LjE1Ljk1IDE5Mi4xNjguMTUuNzMKRklMRSAxOTIuMTY4LjE1LjQ0IDE5Mi4xNjguMTUuOTUgMTkyLjE2OC4xNS43MwpCQUNLVVAgMTkyLjE2OC4xNS40NCAxOTIuMTY4LjE1Ljk1IDE5Mi4xNjguMTUuNzMK</FL>
<FL val="Attach doc_filename">components.txt</FL>
</row>
</JobOpenings>

###XMLDATA Candidates example:
<Candidates>
<row no="1">
<FL val="First name">Satvik</FL>
<FL val="Last name">Kothandaraman</FL>
<FL val="Contact address">my home</FL>
<FL val="Email ID">satvik@advent.com</FL>
<FL val="Contact no">44987654</FL>
<FL val="Total work exp (year)">5</FL>
<FL val="Total work exp (month)">5</FL>
<FL val="Current job title">SE</FL>
<FL val="Skill set">Java</FL>
<FL val="Resume status">New</FL>
<FL val="Attach resume"> TVlTUUwgMTkyLjE2OC4xNS40NCAxOTIuMTY4LjE1Ljk1IDE5Mi4xNjguMTUuNzMKRklMRSAxOTIuMTY4LjE1LjQ0IDE5Mi4xNjguMTUuOTUgMTkyLjE2OC4xNS43MwpCQUNLVVAgMTkyLjE2OC4xNS40NCAxOTIuMTY4LjE1Ljk1IDE5Mi4xNjguMTUuNzMK</FL>
<FL val="Attach resume_filename">components.txt</FL>
</row>
</Candidates>

###The file attachment should be base64encoded and send to us. Along with the name of the file in a separate xml node with fieldlabel_filename as below example:
<FL val="Attach resume"> TVlTUUwgMTkyLjE2OC4xNS40NCAxOTIuMTY4LjE1Ljk1IDE5Mi4xNjguMTUuNzMKRklMRSAxOTIuMTY4LjE1LjQ0IDE5Mi4xNjguMTUuOTUgMTkyLjE2OC4xNS43MwpCQUNLVVAgMTkyLjE2OC4xNS40NCAxOTIuMTY4LjE1Ljk1IDE5Mi4xNjguMTUuNzMK</FL>
<FL val="Attach resume_filename">components.txt</FL>

###Response Format:
<response uri="/ats/private/xml/JobOpenings/addRecords">
<result>
<message>messageRecord(s) added successfully</message>
<recorddetail>
<FL val="Id">54290000000089027</FL>
</recorddetail>
</result>
</response>

 
