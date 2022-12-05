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
The Above four CWEs were mitigated using EscapeShellArgs and EscapeShellCommands. ![Git Ref](https://github.com/kacperszurek/exploits/blob/master/GitList/exploit-bypass-php-escapeshellarg-escapeshellcmd.md) ![Code Reference](https://user-images.githubusercontent.com/100978590/205633037-2a5dcbad-d029-429f-802e-58b2c4b7b21d.png)
#### [CWE 209	Generation of Error Message Containing Sensitive Information](https://cwe.mitre.org/data/definitions/209.html)
No Echo statements in any of the Catch, instead they are using Syslogs to save logs files in the server

#### [CWE 211	Externally-Generated Error Message Containing Sensitive Information](https://cwe.mitre.org/data/definitions/211.html)
There is no SQL query disclosure when we test that web application.
#### [CWE 434	Unrestricted Upload of File with Dangerous Type](https://cwe.mitre.org/data/definitions/434.html)
Sometimes they are checking the type and sometimes they are not.
#### [CWE 453	Insecure Default Variable Initialization](https://cwe.mitre.org/data/definitions/453.html)
Not found anything
#### [CWE 454	External Initialization of Trusted Variables or Data Stores](https://cwe.mitre.org/data/definitions/454.html)
Not found anything
#### [CWE 457	Use of Uninitialized Variable](https://cwe.mitre.org/data/definitions/457.html)
Hard to detect as there are many variables.
#### [CWE 470	Use of Externally-Controlled Input to Select Classes or Code ('Unsafe Reflection')](https://cwe.mitre.org/data/definitions/470.html)
User cannot supply the name of the class manually to get an object.
#### [CWE	473	PHP External Variable Modification](https://cwe.mitre.org/data/definitions/473.html)

#### [CWE	474	Use of Function with Inconsistent Implementations](https://cwe.mitre.org/data/definitions/474.html)
#### [CWE	484	Omitted Break Statement in Switch](https://cwe.mitre.org/data/definitions/484.html)
All Switch statements have break statemants in them.
#### [CWE	502	Deserialization of Untrusted Data](https://cwe.mitre.org/data/definitions/502.html)
Admin could be exploited through serialized object.
#### [CWE	595	Comparison of Object References Instead of Object Contents](https://cwe.mitre.org/data/definitions/595.html)
#### [CWE	616	Incomplete Identification of Uploaded File Variables (PHP)](https://cwe.mitre.org/data/definitions/616.html)
Not Saving the files to global variables.

### Summary of Key Findings



### Project Task Board

[Github Project Page](https://github.com/users/SreeharshaMorampudi/projects/3/views/1)
