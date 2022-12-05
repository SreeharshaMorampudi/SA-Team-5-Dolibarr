# Code Analysis for Software Security Engineering

### Code Review Strategy:  
We choose to employ both an automated and manual analytical strategy for the Dolibarr's code review to find any flaws that could result in serious security problems. We took into account the regions where security is crucial while examining the code. So for this we have decided to use CWE checklist for manual code review and SonarQube for Automatic Code Review. There are many different tools but most of them don't scan PHP code as SonarQube or SonarCloud does.  

### Automated Code Review

The links provided below will take you to the reports the scanning tool produced. SonarQube is used for automatic code analysis to uncover some isseus and vulnerabilities in the software, as was previously discussed. SonarQube supports PHP core scanning in addition to a large number of other programming languages. With the use of this tool, we are able to identify 11 critical flaws that mainly affect XML parsing, cryptographic algorithms, password requirements, and certificate validation. 


#### Report Links

[SonarQube Report](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Code%20Analysis/SonarQube%20Report.md)

### Manual Code Review  
As we mentioned earlier, we have decided to manually review the code using the most regular Comman Weaknesses in Softwares that are written in PHP which are available in CWE website. Our Findings on some of those are listed below.  

### Summary of Key Findings



### Project Task Board

[Github Project Page](https://github.com/users/SreeharshaMorampudi/projects/3/views/1)
