A) CONTENT DESCRIPTION:
 
 A - 1) In General
 In this repository you will find 7 json data files. As you know, json is a {"key" : "value"} fields file. All the value part must be populated wiht data coming from openMRS. 
 In some value parts you could find the name of the data element in DHIS2 to permit you to easy find the right matching concept. But replace this data element name by the right value. 
 In addition you could find in value part something like "UID_toGetByRequest". That's mean you must une a specific JS function to get the right value. These functions will be also available in this repository for each key. 
 
 THE VALUE PART FORMAT:
   - All the date value must be in this format: "yyyy-mm-dd".
   - All the numeric value must be written without any quotes : 10 or 190
 
 Below are the decriptions and the usage of these files. In order:
 
 A - 2) 1st Json File: createNewTrackedEntityInstance:
 This json file is used to create a new tracked entity (a patient, a person) with particular mandatory informations named Attributes.
