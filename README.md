# hl7-fhir-portfolio
HL7 v2 to FHIR integration using Mirth Connect, HAPI FHIR, and Docker
HL7 to FHIR ADT Transformation (Mirth Connect + HAPI FHIR)
This project demonstrates a real-world HL7 v2 ADT^A01 → FHIR Patient transformation using Mirth Connect and a local Docker-based HAPI FHIR server.

# Technologies
Mirth Connect 4.5.2
HAPI FHIR Server (Docker)
HL7 UltraPort Ad Hoc Sender
Postman

# Use Case
Accept HL7 ADT^A01 over TCP
Transform to FHIR Patient JSON
Send to HAPI FHIR server

# Getting Started
Start HAPI server on port 8081 using Docker.
Import Mirth channel (HL7_ADT_to_FHIR_Patient.xml)
Start Mirth on port 8080
Use UltraPort to send adt_sample.hl7 to TCP port 6001
Validate data in HAPI at http://localhost:8081/fhir/Patient

# Send Sample HL7 Message
Use UltraPort or any TCP HL7 sender to send the contents of samples/adt_sample.hl7 to:

Host: localhost
Port: 6001
Validate in HAPI
Check created Patient resources:

GET http://localhost:8081/fhir/Patient
Test with Postman
Import postman/HAPI_FHIR_Test_Collection.json
Includes a GET request to list all Patient resources.

# Sample Message
See samples/adt_sample.hl7 for the ADT^A01 message used.

# Author
Built by Quen R to showcase real-world HL7 → FHIR interoperability.
