A) CONTENT DESCRIPTION:
 
 A - 1) In General
 In this repository you will find 7 json data files. As you know, json is a {"key" : "value"} fields file. All the value part must be populated wiht data coming from openMRS. 
 In some value parts you could find the name of the data element in DHIS2 to permit you to easy find the right matching concept. But replace this data element name by the right value. 
 You will need a "username" and a "password" to connect to DHIS2 instance and then work with the APIs.
 
 THE VALUE PART FORMAT:
   - All the date value must be in this format: "yyyy-mm-dd".
   - All the numeric value must be written without any quotes : 10 or 190
 
 Below are the decriptions and the usage of these files. In order:
 
 A - 2) 1st Json File: createNewTrackedEntityInstance:
 This json file is used to create a new tracked entity (a patient, a person) with particular mandatory informations named Attributes.
 
 The endpoint to use is "http://DHIS2-SERVER-IP/api/trackedEntityInstances" to create new by sending a POST request or this endpoint "http://DHIS2-SERVER-IP/api/trackedEntityInstances/anInstanceID" to edit an existing instance by sending a PUT request.
