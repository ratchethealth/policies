# Introduction

Ratchet Technologies, Inc ("Ratchet") is committed to ensuring the confidentiality, privacy, integrity, and availability of all electronic protected health information (ePHI) it receives, maintains, processes and/or transmits on behalf of its Customers. As providers of compliant, hosted infrastructure used by health technology vendors, developers, designers, agencies, custom development shops, and enterprises, Ratchet strives to maintain compliance, proactively address information security, mitigate risk for its Customers, and assure known breaches are completely and effectively communicated in a timely manner. The following documents address core policies used by Ratchet to maintain compliance and assure the proper protections of infrastructure used to store, process, and transmit ePHI for Ratchet Customers.

Ratchet provides secure and compliant cloud-based software for patient engagement. 

## Ratchet Organizational Concepts

The physical infrastructure environment is hosted at AWS [Amazon Web Services](http://aws.amazon.com). The network components and supporting network infrastructure is contained within AWS infrastructure and managed by AWS. Ratchet does not have physical access into the network components. The Ratchet environment consists of Tomcat web servers, Grails application servers, Java virtual machines and Postgresql database servers, Logstash logging servers, Linux Ubuntu servers, Salt server and OSSEC IDS services.

Within the Ratchet Platform, all data transmission is encrypted and all hard drives are encrypted so data at rest is also encrypted; this applies to all servers - those hosting databases, APIs, log servers, etc. Ratchet assumes all data *may* contain ePHI, even though our Risk Assessment does not indicate this is the case, and provides appropriate protections based on that assumption.

Additionally, AWS's security group is used on each each server for logical segmentation. The security groups are configured to restrict access to only justified ports and protocols. Ratchet has implemented strict logical access controls so that only authorized personnel are given access to the internal management servers. The environment is configured so that data is transmitted from the load balancers to the application servers over an SSL encrypted session.

The web server host are externally facing and accessible via the Internet. The database servers, where the ePHI resides, are located on the internal Ratchet network and can only be accessed directly over an SSH connection by hosts in the Application Security Group. The access to the internal database is restricted to a limited number of personnel and strictly controlled to only those personnel with a business justified reason. Remote access to the internal servers is not accessible except through the load balancers and Salt Master host.

## Version Control

Policies were last updated February 10th, 2016.
