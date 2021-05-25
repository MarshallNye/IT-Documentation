# OVERVIEW
    Disaster Recovery are policies, documentation, and practices that support our ability to remain operational after an adverse event. 
    The goal of DRP is to limit risk and get IT Infrastructure running as close to normal as possible after an unexpected interruption. 
    These practices enable us to get back on our feet after problems occur, reduce the risk of data loss and reputational harm, and improve operations while decreasing the chance of emergencies.
    This document is designed to be used in conjunction with the BCDR Plan. If there is any contradiction between the two documents, the BCDR shall be considered correct.

# WHERE THIS DOCUMENT IS LOCATED
    The DRP source document will be located on the XXXXX Confluence Page.     
    Secondary copies will be made to XXXXXXXXXX
    A physical copy will be printed and kept in a binder labeled “DISASTER RECOVERY PLAN”. This shall be kept in the XXXXX room, within the fire-proof filing cabinet.

# SERVICE CLASSIFICATIONS 
## BLOCKERS - Systems that need to be recovered before you can begin restoring other services. 
Think of Internet access, firewalls, core switching and routing, DNS, Domain Services. Things that, if broken, literally nothing else works.
Domain controllers should be here, if all DCs are affected by an outage. 
RPO: 
RTO:

## CRITICAL - Services that are absolutely critical for business functions. 
Traditionally Accounting, HR, and Payroll systems should be prioritized. The company must be able to take in money, and pay its employees. Who cares if Engineering can make a widget, if they aren't getting paid...
RPO: 
RTO:    

## MEDIUM - Services that enable the organization to produce value. 
Engineering systems, CRM systems, Education Management systems. You should also include any backup systems that could be effected by a disaster scenario.
RPO: 
RTO:

## LOW - Services that can wait to be brought online. 
Ancillary monitoring services, help desks, anything that can wait until we get our LOB applications running
RPO: 
RTO:

# ASSETS
    List all of your servers, infrastructure, services. Do you have service contracts? Who are your vendors?        

# DR TEAM
    Who does what? Phone numbers, email, pagers, carrier pigeons


# DATA BACKUP SYSTEMS
## Overview
        We are utilizing a combination of XXXXXX, Local Storage, XXXXX and XXXXXX for backup and recovery. 
        XXXX handles orchestration and execution of backups, local storage at XXXXXXXX is used for primary/secondary storage 
        XXXXXXX is a cloud storage provider for long term, off-site storage
        XXXXXXXXX is used for offsite DR VM recovery platform

## Server Backups
        Backups of servers are made nightly using XXXXXXXX, running on XXXXXXXX
        The most recent backups are stored on-site within XXXXXXXXXXX Repository
        After a new backup is made, the old backup is automatically transferred to XXXXXXX Cloud Storage

## Network Switch Backups
        All network switches' configurations have been backed up to XXXXXXXXXX and are stored at \\XXXXXXXXXXX

## Firewall Backups
        The Firewall configuration is backed up to XXXXXXXXXX and is stored at \\XXXXXXXXXX

# ASSEMBLY POINTS
    This DRP invocation plan identifies two assembly points. DR Team will report to the Primary Assembly is not viable, members will report to the Secondary Assembly Point    
    
## Primary Assembly Point
        IT Department office

## Secondary Assembly Point
        Secondary Office Breakroom

# RECOVERY LOCATIONS
    Define locations that you can bring equipment and can begin recovery operations.
    Check cooling and electrical capacities of the locations

# AUTHENTICATION AND ACCESS
## Authentication Mechanisms
        Password Manager?
        Local Accounts' Usernames (NO PASSWORDS DUMMY) used in key services (in case AD is broken/unavailable)

## Access Mechanisms
        RDP?
        SSL-VPN?
        Web Management?


# DR RESPONSE PROCESS
## EVALUATE
Detect Incident(s)
Assess severity
Assess Impact

## MITIGATE (Immediately)
What steps need to be taken IMMEDIATELY to reduce the spread of the issue? (Cutting power to a room, turning on emergency A/C units) 
Perform emergency measures to prevent the incident from worsening. 
These measures may be more disruptive than the actual event, but should be viewed as an “amputate the arm to save the patient” situation where the goal is to prevent further damage

## ACTIVATE	
Declare disaster event
Activate DR Team.

## COMMUNICATE
Communicate that there is a disaster, to all affected stakeholders
Communicate the recovery plan
Provide ongoing status updates
Contact relevant authorities or government agencies

## INVESTIGATE
If possible, gather additional information about the situation, to refine the recovery and response process
Provide recovery time table
Gather information about the issue. Not all of these are applicable, mind you. These are to help jog your memory
### WHO 
Was the last person to interact with the system? Physical/Virtual access?
### WHAT 
What services are impacted, what is the scope of the issue?
### WHEN 
Do we know how long this has been going on for? Do we know how long causative conditions will remain?
### WHERE 
Is this distributed, or localized to one are?
### HOW 
Do we know how the event happened?

## RECOVERY
### REMEDIATION
Deploy measures to prevent the issue from worsening. 
These should be steps to restore BLOCKERS  
Any mitigation steps that were taken immediately, consider reverting those once you have stability. 
(Gracefully powering off servers, deploying generators)
### INTERMEDIARY
Deploy intermediary remedies. These may be in place for extended periods of time. (Restore backups to secondary locations. Use backup switches to restore data connectivity)
### PERMANENT
Deploy permanent fixes. These are to bring you back to a point prior to the disaster, and may take some time to implement. (Replace the damaged servers, replace the switches damaged)

## REVIEW
Conduct a post-mortem of the event
Do we have the means to prevent it from happening again?
What went well?
What could have gone better?
Remember, this is should be a no-fault post mortem. If we are afraid of admitting our mistakes, we will never rectify them.

# RELATED ARTICLES

