# Designing for Software Security Engineering
## Threat Modeling
### Data Flow Diagram for Dolibarr CRM
[Data Flow Diagram](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Desingning/DFD.PNG)  
[HTML Threat Model Report](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Desingning/Threat%20Model%20Report.htm) [pdf](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Desingning/ThreatModelReport.pdf)  
## Observations
### Denial of Service Threats  
##### Observations:
One danger we might encounter is from outside parties trying to stop users from exchanging credentials and data with our data repositories. There are several ways to mitigate this, but one essential feature we require is the ability to have admins who can take action like resetting access or creating a new secure location for the exchange to take place in. In order to make sure that all contacts with the databases come from secure sources, automatic monitoring of data retrieval under various credentials via reports or audit logs may also be helpful. Running a corporate VPN on the workstations would also greatly help tackle this problem by keeping outside players out of them.
  
We require two things to combat unexpected crashes and performance problems. System administrators must first be able to cause a restart and restart the system both locally and remotely. In order for the same administrators to quickly identify the problems causing the crashing and take steps to mitigate them going ahead, we also need an error log.
  
At the moment, there is no solution to lessen this problem. One option might be to place a restriction on the number of system requests that each user can make, It wouldn't be a terrible idea to have a means to manually override it from an admin level because a limit like this could result in unduly restricting users and losing usability. Setting a restriction makes it more difficult for outside parties to use our resources maliciously because they can never access all of it at once. Additionally, ensure that timeout is used on every request to a data store so that nothing can continue to pull data indefinitely. This many queries running at once will undoubtedly crash our system.

### Repudiation Threats  
##### Observations:
These threats of repudiation were made while employees were interacting with the Dolibarr system. We were able to find a logging mechanism for employee login attempts in the [documentation] (https://docs.bitnami.com/installer/apps/dolibarr/troubleshooting/debug-errors/). The establishment of a system login log would give the business the ability to monitor the interaction and guarantee the smooth operation of the procedure. The record would also provide information about how the security mechanism operates, confirming that it is effective and revealing any patterns that would need to be anticipated. This log may also be used to monitor employee logins so that it is possible to determine who is logged in and when.  


### Spoofing Threats  
##### Observations:
Since email services depend on third-party software and/or providers, we need to investigate spoofing threats related to them. This includes the data entering and leaving the email system being faked. The unlawful collection of data or its insertion into the data flow or storage would be made possible by these breaches.  

  
### Escalation of Privilege Threats  
##### Observations:
Cross-site request forgery is a problem with escalating privileges that we will need to investigate in relation to the email service because Dolibarr's XSRF protection is documented online, and the email service should also be the one that offers security for email-based conversations.  


## Teamwork  
Despite finishing the work, we had very few problems in our group with task distribution, communication, and follow-through. We did have two meetings for this task, where we spent time analyzing, talking about, and creating the preliminary Data-Flow Diagrams.

These meetings went smoothly and were beneficial to everybody involved. Our weekly check-in meetings with Dr. Robin Gandhi have been very beneficial in resolving all of our questions and improving our design diagrams. At first, we included several processes in a single DFD diagram, which resulted in almost 100 threats. Later, after taking the professor's suggestions into account, we slightly modified the design and were able to document it with better material.  

[Team Project Board](https://github.com/users/SreeharshaMorampudi/projects/3)  

