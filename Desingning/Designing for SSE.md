# Designing for Software Security Engineering
## Threat Modeling
### Data Flow Diagram for Dolibarr CRM
![]()
[HTML Threat Model Report]()
## Observations
### Denial of Service Threats  
Observations:  
One danger we might encounter is from outside parties trying to stop users from exchanging credentials and data with our data repositories. There are several ways to mitigate this, but one essential feature we require is the ability to have admins who can take action like resetting access or creating a new secure location for the exchange to take place in. In order to make sure that all contacts with the databases come from secure sources, automatic monitoring of data retrieval under various credentials via reports or audit logs may also be helpful. Running a corporate VPN on the workstations would also greatly help tackle this problem by keeping outside players out of them.
  
We require two things to combat unexpected crashes and performance problems. System administrators must first be able to cause a restart and restart the system both locally and remotely. In order for the same administrators to quickly identify the problems causing the crashing and take steps to mitigate them going ahead, we also need an error log.
  
At the moment, there is no solution to lessen this problem. One option might be to place a restriction on the number of system requests that each user can make, It wouldn't be a terrible idea to have a means to manually override it from an admin level because a limit like this could result in unduly restricting users and losing usability. Setting a restriction makes it more difficult for outside parties to use our resources maliciously because they can never access all of it at once. Additionally, ensure that timeout is used on every request to a data store so that nothing can continue to pull data indefinitely. This many queries running at once will undoubtedly crash our system.

### Repudiation Threats  
Observations:  

### Spoofing Threats  
Observations:  
  
### Escalation of Privilege Threats  
Observations:  


## Teamwork
[Team Project Board]     
