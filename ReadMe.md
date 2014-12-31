Fuse direct-vm Example
======================

This project contains two OSGI bundles that work together to showcase how to use the direct-vm endpoint in Apache Camel.

Both bundles need to be deployed in a Fuse container for the project to work succesfully.

Project Details:
================
Flow:
-----
exampleHello CXF Webservice -> Simple body transformation -> direct-vm to exampleGoodbye -> Simple body transformation -> Route message back to caller.
Description:
------------
The exampleHello project exposes a simple webservice at http://localhost:8181/cxf/HelloWorld. Whenever a request is received the helloWorld service does some simple Transformations to the request and then makes a direct-vm call to exampleGoodbye, passing along the payload. The exampleGoodbye service performs a simple transform and returns the transformed payload back to exampleHello which returns the final result back to the caller.
