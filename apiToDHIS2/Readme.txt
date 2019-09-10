A) CONTENT DESCRIPTION:
 
 A - 1) In General
 In this repository you will find 7 json data files. As you know, json is a {"key" : "value"} fields file. All the value part must be populated wiht data coming from openMRS. 
 In some value parts you could find the name of the data element in DHIS2 to permit you to easy find the right matching concept. But replace this data element name by the right value. 
 You will need a "username" and a "password" to connect to DHIS2 instance and then work with the APIs.
 
 THE VALUE PART FORMAT:
   - All the date value must be in this format: "yyyy-mm-dd".
   - All the numeric value must be written without any quotes : 10 or 190
 
 Below are the decriptions and the usage of these files. In order:
 
 A - 2) 1st Json File: createNewTrackedEntityInstance.json:
 This json file is used to create a new tracked entity (a patient, a person) with particular mandatory informations named Attributes.
 
 The endpoint to use is "http://DHIS2-SERVER-IP/api/trackedEntityInstances" to create new by sending a POST request 
 or this endpoint "http://DHIS2-SERVER-IP/api/trackedEntityInstances/anInstanceID" to edit an existing instance 
 by sending a PUT request.

 A - 3) 2nd Json File: enrolleTrackedEntityInstance.json:
 This json file is used to enroll a TEI (Tracked Entity Instance) to a specific program.
 In the json file you have to specify the TEI ID, the progam ID, the enrollment date and the incident date.
 
 The endpoint to use is "http://DHIS2-SERVER-IP/api/enrollments" to enroll a new TEI by sending a POST request 
 or this endpoint "http://DHIS2-SERVER-IP/api/enrollments/enrollmentID" to edit an existing enrolled TEI 
 by sending a PUT request.
 
 A - 3) 3rd Json File: createNewEvent*****.json :
 These Json files are used to create events (a form or program stage).
 You must specify into these files the program ID, the organisation unit ID, the event date, the program stage ID,
 the username who record this event, the enrollment ID and all the remaining fields value.
 
 The endpoint to use is "http://DHIS2-SERVER-IP/api/events" to record a new event by sending a POST request 
 or this endpoint "http://DHIS2-SERVER-IP/api/events/eventID" to edit an existing event 
 by sending a PUT request.
