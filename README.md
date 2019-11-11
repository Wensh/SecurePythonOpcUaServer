# SecurePythonOpcUaServer
based on: https://github.com/FreeOpcUa/python-opcua  
Python: 3.7.3 32bit  
OPC UA Library: opcua==0.98.7  

## Description
This is a basic example Server with Sign&Encrypt and Authentication.  
Tested with an Siemens S7-1500 OPC UA Client and my SecurePythonOpcUaClient    
in addition to:  
https://github.com/AndreasHeine/SecurePythonOpcUaClient  
https://github.com/AndreasHeine/PythonOpcUaServer-for-Simatic-S7-1500-OpcUaClient  

## Generate your own Certificate

Step 1: Change ssl.conf (subjectAltname, country, organizationName, ...)  
Step 2: openssl genrsa -out key.pem 2048  
Step 3: openssl req -x509 -days 365 -new -out certificate.pem -key key.pem -config ssl.conf  
