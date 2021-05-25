Scenario Name (ex: Flood of Primary Datacenter)

# Activation Condition(s)
- Flooding event within the server room

# Possible Causes
- Flood
- Accidental Sprinkler activation

# Effected Resources
- SRV-DC01
- SRV-VCSA
- All VMs
- ROUTER-01

# Disaster Ramifications
- High level list of what will happen (ex All email services will be lost)
- Internet connectivity lost
- Application servers lost
- Backup Server appliances and primary backup storage lost
- Domain controllers lost
- VDI resources lost
- DHCP and DNS lost

# Disaster Recovery Obstacles and Mitigation

## Obstacle Title (ex: Recovery Capacity)   

### Summary
- Describe a major obstacle to recovery (ex: Company lacks any capacity to run our server environment anywhere other than the main datacenter. While we have backups of all critical systems, if the datacenter is destroyed we will have no place to restore the backups to.)

### Mitigation Options 
- Describe ways to mitigate or eliminate this obstacle. This should be high level, you can break down these tasks elsewhere (ex: Offsite Disaster Recovery virtualization destination such as Azure, Migrate all or some critical systems to Azure VMs in hybrid deployment)

# DRP Sequence
- This is what we do when this DR Scenario is triggered
    
## EVALUATE 
- Detect Incident(s)
- Assess severity
- Assess Impact
    
## MITIGATE (Immediately)
- Confirm there is no life safety hazard
- Gracefully power off anything that is accessible
- Remove equipment from the server room. Place all equipment in X room.
- Turn on and deploy portable AC units within new temporary room. This will help with heat and moisture.

## ACTIVATE
- Declare disaster event, activating DR Team.
    
## COMMUNICATE (Continuously) 
- Communicate issue to all the stakeholders
- Use backup communication methods if needed.
- Send status updates at set intervals, even if there isn’t new information. Make sure people know the issue is being worked on. 
    
## INVESTIGATE
- Gather history of the event, as applicable
- Investigate the root cause, as applicable
- Find what resources you have currently to remediate? What needs to be ordered/purchased?
- What is an expected timeline on replacement parts, services, or labor?
    
## RECOVERY

### REMEDIATION
#### HQ Internet Access
- Contact ISP for replacement hardware
- Deploy 4G cellular modem and confirm connectivity
#### Firewall
- Order Replacement Firewall
- Deploy firewall
#### Active Directory Access
- Stand up new domain controller in recover location, confirm AD synchronizes with Azure
#### Core Routing and Switching
- do this     
#### DNS
- do that      
#### DHCP
- Confirm DHCP Failover      

#### Backup Orchestration
            
### INTERMEDIARY
#### Initiate Azure Site Recovery  
- step 1
- step 2

### PERMANENT
#### Deploy replacement physical servers
- step 1
- step 2

#### Migrate VMs back on premise

# REVIEW
- Do we have the means to prevent it from happening again?
- What went well?
- What could have gone better?
- Remember, this is should be a no-fault post mortem. If we are afraid of admitting our mistakes, we will never rectify them.