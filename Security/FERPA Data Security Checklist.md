# About PTAC 
The U.S. Department of Education established the Privacy Technical Assistance Center (PTAC) as a “one-stop” resource for education stakeholders to learn about data privacy, confidentiality, and security practices related to student-level longitudinal data systems and other uses of student data. PTAC provides timely information and updated guidance through a variety of resources, including training materials and opportunities to receive direct assistance with privacy, security, and confidentiality of student data systems. More PTAC information is available at https://studentprivacy.ed.gov. PTAC welcomes input on this document and suggestions for future technical assistance resources relating to student privacy. Comments and suggestions can be sent to PrivacyTA@ed.gov. 

# Purpose 
The purpose of this checklist is to assist stakeholder organizations, such as state and local education agencies, with developing and maintaining a successful data security program. A data security program is a vital component of an organizational data governance plan, and involves management of people, processes, and technology to ensure physical and electronic security of an organization’s data. A comprehensive security program is critical to protecting the individual privacy and confidentiality of education records. Solutions and procedures supporting data security operations of education agencies should address their unique challenges, including the need to protect personally identifiable information (PII) while maintaining quality, transparency, and necessary access to the data. To ensure that all aspects of a security plan are executed properly, the program should offer clear guidance and tools for implementing security measures. The summary below lists essential components that should be considered when building a data security program. More information on terms discussed in this checklist is available at https://studentprivacy.ed.gov/glossary. 

# Data Security Checklist 
## Policy and governance
Develop a comprehensive data governance plan that outlines organizational policies and standards regarding data security and individual privacy protection. The plan should clearly identify staff responsibilities for maintaining data security and empower employees by providing tools they can use to minimize the risks of unauthorized access to PII. Refer to PTAC’s Data Governance Checklist for more information. q 

## Personnel security
* Create an Acceptable Use Policy that outlines appropriate and inappropriate uses of Internet, Intranet, and Extranet systems. 
* Incorporate security policies in job descriptions and specify employee responsibilities associated with maintaining compliance with these policies. 
* Conduct regular checks and trainings to ensure employee understanding of the terms and conditions of their employment. 
* Confirm the trustworthiness of employees through the use of personnel security screenings, policy training, and binding confidentiality agreements. PTAC-CL-2, December 2011 (revised July 2015) 2

## Physical security
Make computing resources physically unavailable to unauthorized users. This includes securing access to any areas where sensitive data (i.e., data that carry the risk for harm1 from an unauthorized or inadvertent disclosure) are stored and processed, such as buildings and server rooms. An unlocked server room is an invitation for malicious or accidental damage. Monitor access to these areas to prevent intrusion attempts (e.g., by administering identification badges and requiring staff and visitors to log in prior to entering the premises or accessing the resources).

## Network mapping
Network mapping provides critical understanding of the enterprise (servers, routers, etc.) and its connections. Furthermore, network mapping can capture applications and associated data. A robust mapping capability will map the dependencies between applications, data, and network layers, and highlight potential vulnerabilities. There are a number of network mapping tools available.

## Inventory of assets
The inventory should include both authorized and unauthorized devices used in your computing environment. These devices are often scanned and discovered by automated programs (continuously searching the internet for vulnerabilities) and if unsecured devices are discovered they can be compromised. Inventorying, when used in conjunction with network mapping, will give your organization a better understanding of the security requirements needed to protect your assets. q 

## Authentication
The ways in which someone may be authenticated fall into three categories: something you know, something you have, or something you are. Two-factor authentication (TFA) combines two of these elements and is more costly, but provides more security. Consider TFA for remote users or privileged “super users.” Authentication technologies provide assurance that the person is authorized to access network assets, services, and information.

## Provide a layered defense
Employ a “Defense in Depth” architecture that uses a wide spectrum of tools arrayed in a complementary fashion. The most common layers to protect are hosts (individual computers), application, network, and perimeter. There are specific security controls that are suited for use at each of these layers. Relying on a firewall alone to protect your network is never adequate.

## Secure configurations
It is a best practice not to put any hardware or software onto your network until it has been security tested and configured to optimize its security. Continuous scanning to ensure system components remain in a secure state is a critical capability that will enhance data security protection. Proactive management of security risks also involves establishing a comprehensive change management program to analyze and address security and privacy risks introduced by new technology or business processes. 

## Access control
Securing data access includes requiring strong passwords and multiple levels of user authentication, setting limits on the length of data access (e.g., locking access after the session timeout), limiting logical access to sensitive data and resources, and limiting administrative privileges. Role-based access is essential for protecting PII and sensitive data; 1 Here, harm refers to any adverse effects that would be experienced by an individual whose PII was the subject of a loss of confidentiality, as well as any adverse effects experienced by the organization that maintains the PII (NIST, Guide to Protecting the Confidentiality of Personally Identifiable Information (PII), 2010 Special Publication 800-122, p. 3-1, 2). Harm to an individual includes any negative or unwanted effects (i.e., that may be socially, physically, or financially damaging). PTAC-CL-2, December 2011 (revised July 2015) 3 defining specified roles and privileges for users is a required security procedure. Sensitive data that few personnel have access to should not be stored on the same server as other types of data used by more personnel without additional protections for the data (e.g., encryption). 

## Firewalls and Intrusion Detection/Prevention Systems (IDPS)
A firewall is a device designed to permit or deny network transmissions based upon a set of rules. Firewalls are frequently used to protect networks from unauthorized access, while permitting legitimate communications to pass. An IDPS is a monitoring device that is designed to detect malicious activity on the network. Although some automatically take remediation action, most report suspicious activity to a central monitoring point for further analysis. 

## Automated vulnerability scanning
When new vulnerabilities (to hardware, operating systems, applications, and other network devices) are discovered, hackers immediately scan networks for these vulnerabilities. Scanning your network and systems on a regular basis will minimize the time of exposure to known vulnerabilities.

## Patch management
Patch management is the process of using a strategy and plan for the testing and roll out of software updates and patches on a regular basis. The plan should address how patches will be applied to which systems at a specified time. A patch is a piece of code that protects computers and applications by updating the security state against new threats or vulnerabilities. Used in conjunction with vulnerability scanning, the enterprise can quickly shut down any vulnerability discovered. 

## Shut down unnecessary services
Each port, protocol, or service is a potential avenue for ingress into your enterprise. A best practice, which should be part of a secure configuration, should include shutting down all services and ports that are not required in your computing environment. A secure enterprise will continually monitor for the use of unapproved ports, protocols or services. 

## Mobile devices
When sensitive data are stored on servers or on mobile devices, such as laptops or smart phones, the data should be encrypted. There are far too many examples of mobile devices being lost or stolen and the subsequent exposure of the sensitive information stored on those devices in the public domain.

## Emailing confidential data
Consider the sensitivity level of the data to be sent over the email. Emailing unprotected PII or sensitive data poses a high security risk. It is recommended that organizations use alternative practices to protect transmissions of these data. These practices include mailing paper copies via secure carrier, de-sensitizing data before transmission, and applying technical solutions for transferring files electronically (e.g., encrypting data files and/or encrypting email transmissions themselves). q Incident handling. When an incident does occur it is critical to have a process in place to both contain and fix the problem. Procedures for users, security personnel, and managers need to be established to define the appropriate roles and actions. Outside experts may be required to do a forensics investigation of the incident, but having the correct procedures in place initially will minimize the impact and damage. 

## Audit and compliance monitoring
Audits are used to provide an independent assessment of your data protection capabilities and procedures (see Data Stewardship: Managing Personally PTAC-CL-2, December 2011 (revised July 2015) 4 Identifiable Information in Electronic Student Education Records) and should be performed periodically. Auditors that are familiar with Family Educational Rights and Privacy Act statutory and regulatory requirements can further assist you in determining whether your systems are in compliance.