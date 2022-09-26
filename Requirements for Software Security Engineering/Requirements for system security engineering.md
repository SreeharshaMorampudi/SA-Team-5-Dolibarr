# Requirements for System Security Engineering

## Index
### SECTION ONE
* **[Access Customer Profiles and Transactions](#case-1)**
* **[Share Log Files and Documents](#case-2)**
* **[Attack by Installing Add-Ons](#case-3)**


### SECTION TWO
* **[Security Related Configuration and Installation Issues](#security-related-configuration-and-installation-issues)**
* **[Reflection](#reflection)**
* **[Sources](#sources)**

## SECTION ONE

### Case 1
#### Accessing customer profiles and transactions

#### Use Case
Bank Teller needs access to the customer's profile and transactions whenever an existing customer comes into the bank. The bank teller needs to log into Dolibarr to view profiles. To create a secure login to the system, he should type in the username and password.  

#### Misuse Case
The goal of the hacker is to obtain unauthorized access to the server and steal private customer data. To access the system, he might employ brute-force attacks, session hijacking, dictionary attacks, key loggers, and credential stuffing.  

#### Prevention and Security Requirement
These attacks can be prevented by implementing the following features:
1.	 Progressive Delays using Captcha/limiting the maximum number of attempts  
2.   Session Validation  
3.   Strong Passwords  
4.   Multifactor Authentication  
5.   Password management  

### UML Diagram
![Case1 Diagram](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Requirements%20for%20Software%20Security%20Engineering/usecase1final.drawio.png) 


#### Alignment of Security Requirements with Advertised Features
* Dolibarr provides progressive delays during login by implementing the CAPTCHA
* Dolibarr provides Session timeouts and session expiry after logout
* Dolibarr provides strong password recommendations, and also provides a strong password by using its algorithm
* Dolibarr doesn't provide any multi-factor-authentication
* Access can be restricted and force users to change the password after a specified date.

### Case 2
#### Sharing Files and Documents

#### Use Case
A bank teller is working in a bank and uses Dolibarr as their ERP and CRM application to manage their business. They have different types of accounts that are offered to their customers as a part of their business. One day a client who is part of a partnership group account walks into the bank and asks the bank teller to share the log records of their bank account by stating the reason that he wants to review and monitor some of the suspicious activity that is going on on their account. As he is already in the bank, he also wants to apply for a top-up loan for their partnership firm to expand their business. For this, there are a couple of documenting procedures to be carried out where the signatures of the client and his partners are required. The banker has asked to give him some time to pull up the required documents to be signed and also the log records. The banker has shared the documents with the customer via a shared link.

#### Misuse Case
There is one partner in the client's business who is already a member of the group account. He has made some money withdrawals and transfers for his personal use and wants to hide them from the logs that the banker has shared with another partner. So, he hired a hacker from outside to do this. Somehow he also came to know that his partner is going to apply loan for their business. So the partner with bad intentions wants the hacker to change his liability of repaying the loan to zero or minimum share. Hacker then performs log tampering to hide modifications and modify the loan agreement to change the terms of the agreement as asked by his recruiter. 

#### Prevention and Security Requirement
To overcome these attacks the following security features should be implemented. They are:  
1.	 Inclusion of attributes  
2. Password-protected files
3.   Docusign for signing the documents 

### UML Diagram
![Case2 Diagram](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Requirements%20for%20Software%20Security%20Engineering/Usecase2final.drawio.png)


#### Alignment of Security Requirements with Advertised Features
* Dolibarr follows a different type of log protection to make them unalterable.
     * https://wiki.dolibarr.org/index.php/Module_Unalterable_Archives_-_Logs
* Dolibarr doesn't support built-in password-protecting documents but can implement using third-party plug-ins.
* Documents can be shared using DocuSign to maintain high security to the files shared for collecting a signature. This feature plug-in can be added from Dolistore Marketplace.
	* https://www.dolistore.com/en/



### Case 3
#### Share Login links to the employees

#### Use Case
Being a bank with several customers, Banker has to recruit staff to manage their business. In this process, Banker has to create users in the Dolibarr system and assign some tasks to them which allows access to customers and other important information. As the creation of users also involves provisioning of access to the employees, the banker has to share a welcome email from Dolibarr along with the Password reset link and link to login into the system. 

#### Misuse Case
A hacker employed by a competing bank seeks to get illegal access to the server to collect secret information about the bank's credit policies. To access the other sensitive information, he tries to change links.

#### Prevention and Security Requirement

Few security features to keep the supervisor system secure from attackers are as follows:
1.	The traffic with an email containing links should be protected with TLS. 
2.	The links should be encrypted.

### UML Diagram
![Case3 Diagram](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Requirements%20for%20Software%20Security%20Engineering/usecase02.drawio.png)


#### Alignment of Security Requirements with Advertised Features
* Dolibarr uses TLS to encrypt the communications that are happening over email.
     * https://wiki.dolibarr.org/index.php/Setup_EMails


## SECTION TWO

### Security Related Configuration and Installation Issues

*	Documentation from Dolibarr about the security-related features:
    * https://wiki.dolibarr.org/index.php?title=Security_information
*	Documentation from Dolibarr to set up secure email communications from the system:
	* https://wiki.dolibarr.org/index.php/Setup_EMails
*	Documentation from Dolibarr on their Security policy and scope for possible vulnerabilities and contributions:
	* https://github.com/Dolibarr/dolibarr/blob/develop/SECURITY.md



### Reflection

Each of the three team members contributed a scenario and use case diagram. Before and after our instructor check-in, we had two meetings to go through the project. To stay on task, we used a [Project Board](https://github.com/users/SreeharshaMorampudi/projects/3) and Slack for communication. We intended to finish our tasks with enough time for each team member. Given that we are all new to this kind of modeling, there have been a lot of discussions. We worked well as a team to complete both of these team project submissions, but we were always looking for ways to get better for the following round.

Individual Contributions:
* Sreeharsha Morampudi: Building Use case diagrams and changing making a few modifications to teammates’ diagrams, Analyzing the security issues, Documenting the Requirements for SSE and sharing it on GitHub, scheduling Team meetings, and dividing the tasks.
* Saahas Tej Thurpu: Building Use case diagrams, team reflection, organization, task delegation, review use cases, and diagrams, attend team meetings and discuss scenarios.
* Khedir Qasim: Use cases and diagram reviewing. Review the documentation and design of the document, attend team meetings and discuss scenarios.  

### Sources

* https://www.oreilly.com/library/view/network-security-hacks/0596006438/ch01s06.html
* https://www.docusign.com/trust/security/product-security
* https://wiki.dolibarr.org/index.php?title=Security_information
* https://wiki.dolibarr.org/index.php/Setup_EMails


###### [Return to Top](#requirements-for-system-security-engineering)
