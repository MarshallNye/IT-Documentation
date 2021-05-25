# GATHER INFORMATION
1. Identify current BC/DR strategies and policies, if any exist.
- Does the existing plan cover technology related incidents? 
- Do you have 3-2-1 backups? Are they good? Are they tested?
- Identify backup and off-site storage procedures
- What capacity do you have to restore services to an alternate site? 
- Are you able to leverage DRaaS?

2. Identify and assess disaster risks
- Review the history of unplanned incidents and outages, and how they were handled
- Check for historic data on natural disasters in the area. https://msc.fema.gov/portal/home
- Which Electric Grid are you on? If you have multiple locations, are they on different ciruits?
- Does anyone remember the last major incident, and was anything learned from it?

3. Define the worst possible disaster that a company can survive
- Use this scenario as the worst-case, which will impact the most systems. This will probably be a regional disaster where you lose all sites simultaneosly. Nuclear Armageddon, while exciting, is excessive. 

4. Inventory your assets (applications, servers, infrastructure and resources)
- What is the business impact of each asset?
- How difficult is each system to restore?
- How much redundancy and availability already exists? 

5. Identify System Stakeholders
- Traditionally these would be department heads site managers. People who must be notified in the case of an emergency. These people should be made aware of the disaster recovery plan

6. Ballpark the current RTO and RPO goal for each of the disaster scenarios. 
- Does management understand how long a DR process can take? What is the acceptable loss of income/productivity they CAN withstand?
- How much downtime do they WANT to withstand? (HINT: They will always say 0)

# PLAN
1. Create a DR Team
- This could just be you and the IT Team, but should include higher ups who can disseminate information to other departments and teams

2. Make a copy of the DR Threat Matrix in this repository

3. Add all of your assets as rows on the DR Threat Matrix

4. Add each of your Disaster Scenarios as new columns on the DR Threat Matrix

5. Prioritize assets by importance. After BLOCKERS, work with your stakeholders to define the importantance of each asset as reasonable. Label each asset in the 'Category' column on the DR Threat Matrix

**BLOCKERS** Systems that need to be recovered before you can begin restoring other services. 
- Think of Internet access, firewalls, core switching and routing, DNS, Domain Services. Things that, if broken, literally nothing else works.
Domain controllers should be here, if all DCs are affected by an outage. 

**CRITICAL** Services that are absolutely critical for business functions. 
- Traditionally Accounting, HR, and Payroll systems should be prioritized. The company must be able to take in money, and pay its employees. Who cares if Engineering can make a widget, if they aren't getting paid...

**MEDIUM** Services that enable the organization to produce value. 
- Engineering systems, CRM systems, Education Management systems. You should also include any backup systems that could be effected by a disaster scenario.

**LOW** Services that can wait to be brought online. 
- Ancillary monitoring services, help desks, anything that can wait until we get our LOB applications running

6. Define the restore order for BLOCKERS. Add the order number under 'Restore Order'
- In the worst case, what order do you need to restore BLOCKERS in order to restore anything else. 

7. At the intersection of each asset and scenario, define the impact of the disaster on the service. The included excel has color coding because we're fancy.
**X** Asset/service rendered completely non-functional
**D** Degraded functionality, where you have some redundancy inplace
**H** Systems with high availability, where the disaster may effect a component, but the overall system will experience no issue.
**G** Good/no issue in the scenario   

8. For each asset, define mitigation and remediation steps

**Mitigation steps**
- This step is going to take some time. 
- Identify what is needed to bring the asset to an acceptable level of resiliency. 
- The goal is to get all of our boxes to at least D, preferrably H.
- There may be more that one solution.
- Find the costs of the proposed mitigation steps
- Estimate how long it will take to implement each option?
- Estimate the impact on RTO and RPO

**Remediation steps**
- Define what you will need to do to bring assets back online after an incident.

9. Create an implementation roadmap.
- Order the mitigation steps by balancing implementation speed, criticality, and current redundancy
- You may not choose to implement all of your options. You're balancing needs, impact cost, and time.  
- Systems that have 0 redundancy may be weighted higher than more “important” systems that have good redundancy 

10. Define DRP playbooks for the major incident types.
- Use the Scenario Template in this repository for a starting point 
- You can keep things general at first: ‘Loss of Primary Datacenter’ can cover the events of a fire, flood, or earthquake, for example. 
- If there are special considerations for each threat type, you can specify them explicitly. 

# IMPLEMENT
1. Have management review and approve the DRP. Show them current and projected RPO/RTO 
2. Create and distribute multiple copies of the DRP
3. Implement mitigation steps. This might take a long time.

# TEST AND IMPROVE

1. Once you have completed a mitigation step, review the impact of it on your DR plans. Update accordingly.
2. Test the plan. Work within your organization to test. Run a tabletop, simulate an outage, hire a chaos monkey
3. Review the plan at least annually
