# Code Analysis for Software Security Engineering

### Code Review Strategy:  
We choose to employ both an automated and manual analytical strategy for the Dolibarr's code review to find any flaws that could result in serious security problems. We took into account the regions where security is crucial while examining the code. So for this we have decided to use CWE checklist for manual code review and SonarQube for Automatic Code Review. There are many different tools but most of them don't scan PHP code as SonarQube or SonarCloud does.  

### Automated Code Review

The links provided below will take you to the reports the scanning tool produced. SonarQube is used for automatic code analysis to uncover some isseus and vulnerabilities in the software, as was previously discussed. SonarQube supports PHP core scanning in addition to a large number of other programming languages. With the use of this tool, we are able to identify 11 critical flaws that mainly affect XML parsing, cryptographic algorithms, password requirements, and certificate validation. 


#### Report Links

[SonarQube Report](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Code%20Analysis/SonarQube%20Report.md)

### Manual Code Review  
As we mentioned earlier, we have decided to manually review the code using the most regular Comman Weaknesses in Softwares that are written in PHP which are available in CWE website. Our Findings on some of those are listed below.  
#### [CWE	88	Improper Neutralization of Argument Delimiters in a Command ('Argument Injection')](https://cwe.mitre.org/data/definitions/88.html)
#### [CWE 95	Improper Neutralization of Directives in Dynamically Evaluated Code ('Eval Injection')](https://cwe.mitre.org/data/definitions/95.html)
#### [CWE 96	Improper Neutralization of Directives in Statically Saved Code ('Static Code Injection')](https://cwe.mitre.org/data/definitions/96.html)
#### [CWE 98	Improper Control of Filename for Include/Require Statement in PHP Program ('PHP Remote File Inclusion')](https://cwe.mitre.org/data/definitions/98.html)
The Above four CWEs were mitigated using EscapeShellArgs and EscapeShellCommands.  [Git Ref](https://github.com/kacperszurek/exploits/blob/master/GitList/exploit-bypass-php-escapeshellarg-escapeshellcmd.md) 
![Code Reference](https://user-images.githubusercontent.com/100978590/205633037-2a5dcbad-d029-429f-802e-58b2c4b7b21d.png)(![image](https://user-images.githubusercontent.com/100978590/205640849-d09f01b7-81ec-402f-b079-c589b37e6e9d.png))
#### [CWE 209	Generation of Error Message Containing Sensitive Information](https://cwe.mitre.org/data/definitions/209.html)
No Echo statements in any of the Catch blocks, instead they are using Syslogs to save logs files in the server. The developer does not leak sensitive information after catching errors throughout the codebase. ![Barcode.php](https://user-images.githubusercontent.com/100978590/205641382-d5f1a0ed-1668-4129-97e5-7fa6734964da.png)
![Emailcollector.php](https://user-images.githubusercontent.com/100978590/205641482-ca6c92f2-948c-442b-8e33-3ca3354f1b02.png)


#### [CWE 211	Externally-Generated Error Message Containing Sensitive Information](https://cwe.mitre.org/data/definitions/211.html)
There is no SQL query disclosure that has been observed when we test that web application.
#### [CWE 434	Unrestricted Upload of File with Dangerous Type](https://cwe.mitre.org/data/definitions/434.html)
Sometimes they are checking the type and sometimes they are not.
#### [CWE 453	Insecure Default Variable Initialization](https://cwe.mitre.org/data/definitions/453.html)
We are unable to find anything that is related to this CWE.
#### [CWE 454	External Initialization of Trusted Variables or Data Stores](https://cwe.mitre.org/data/definitions/454.html)
We are unable to find anything that is related to this CWE.
#### [CWE 457	Use of Uninitialized Variable](https://cwe.mitre.org/data/definitions/457.html)
Hard to detect as there are many variables.
#### [CWE 470	Use of Externally-Controlled Input to Select Classes or Code ('Unsafe Reflection')](https://cwe.mitre.org/data/definitions/470.html)
User cannot supply the name of the class manually to get an object.
#### [CWE	484	Omitted Break Statement in Switch](https://cwe.mitre.org/data/definitions/484.html)
All Switch statements have break statemants in them.
#### [CWE	502	Deserialization of Untrusted Data](https://cwe.mitre.org/data/definitions/502.html)
#### Admin could be exploited through serialized object.  
getListOfExtrafields() function in the class "htdocs/api/class api_setup.class.php" will call the vulnerable function jsonOrUnserialize().
A normal user could exploit the User Boundary by storing a malicious serialized object in the database which the admin will retrieve that object and execute that leading to code injection. In other words, storing the malicious data could cause privilege escalation for the normal user.
The admin user is vulnerable to deserialized objects by retrieving JSON/Serialized objects from the database. Users could manipulate this object by injecting malicious JSON/serialized objects in the extra field parameter, as shown in the below screenshots. Therefore the returned list will be executed in the admin workspace, causing intentional code injection  
![image](https://user-images.githubusercontent.com/100978590/207442518-4f2fcb19-3934-40ef-9f93-8a80e38ef550.png)
![image](https://user-images.githubusercontent.com/100978590/207442612-c78a2348-1e5f-491e-a5b4-209a8801ae01.png)
![image](https://user-images.githubusercontent.com/100978590/207442730-03010ec8-9d74-444e-a867-fa07b1974cb3.png)

#### [CWE	616	Incomplete Identification of Uploaded File Variables (PHP)](https://cwe.mitre.org/data/definitions/616.html)
Not Saving the files to global variables.
#### [Testing Injection Attacks with old Dataset]()  
![image](https://user-images.githubusercontent.com/100978590/207441007-d73d68ce-e19f-4de5-8c07-16d6e3b95dfd.png)  
There is a function testSqlAndScriptInject in the file htdocs/main.inc.php. This function is used at different places of the software to check if there are any signs of injection attacks.  
Even though they are using this function to check the injections, the datasets that are used are very limited and doesnot cover the latest patterns of Injection attacks. We can refer to XSS scripts on GitHub to get more possible patterns and include them as well to make it more secure.

### Summary of Key Findings  
From the Automated code scanning tools and Manual code review, we can see that there are nothing much severe issues that lead to breaking the functionality of the Dolibarr software, we have found some key issues related to certificate valination, Cryptographic Algorithms that need to be updated as per the latest trends. We are planning to contribute our findings to Dolibarr in updating the scripts to exclude all the vulnerabilities that were identified in our code review.

### Team Collaboration  
Since this assignment was announced during the Thanks Giving Holiday Break, despite vacations we have planned to do the code review of our project. We are able to separate the tasks individually to accomplish this assignment on time. Initially, there was lot of confusion on how to start and where to start with the code review. But Professor's lectures and Team checkin meetings helped us a lot in clearing those doubts and move forward with ease. SonarQube and SonarCloud made our tasks easy by automatically scanning the Dolibarr code repository and detecting all the possible issues. From those results we have divided our tasks equally and worked on this assignment. Our team's great communication and coordination helped in accomplishing this task.

### Project Task Board

[Github Project Page](https://github.com/users/SreeharshaMorampudi/projects/3/views/1)
