# Assurance Cases for Software Security Engineering  

## Assurance Case 1
![Assurance Case 1 Diagram]()


### Evidence 1: Usage of CAPTCHA
Usage of captcha in Dolibarr makes it difficult for hacker to perform multiple login attempts using rendom passwords.  

### Evidence 2: Log Report of multiple unsuccessful attempts and block the IP address
Dolibarr allows Admin to block the IP addresses that he founds to be suspicious with multiple unsuccessful login attempts.  

### Evidence 3: Time based OTP
Using Two-Factor Authentication, Dolibarr sends a One Time Password to be entered by the user so that even if Hacker knows the login details he cannot login to the system.  

### Evidence 4: Strong Password Policy
Dolibarr has rules to make strong passwords to the users so that users need not to worry about dictionary attacks.  

### Evidence 5: Strong Password Management policy
In Dolibarr Admin can refresh the user's password anytime or time to time so that even the passwords are leaked in a data breach, Hackers can be prevented to login in to the system.  


## Assurance Case 2
![Assurance Case 2 Diagram]()

### Evidence 1: Docusign Security Feature
By implementing Docusign Module in Dolibarr, the documents can be shared only to the intended users so that no modifications or false confirmations can be avoided by hackers.

### Evidence 2: Log Report on File modifications
As the files shared will be read only, any attempts of changes in the files can be found using the log report on file modifications.  

### Evidence 3: Man in the middle report
As files are shared using links, All communications to and from Dolibarr are secured because TLS/SSL is used.  


## Assurance Case 3
![Assurance Case 3 Diagram]()

### Evidence 1: Counter SQL Injection/XSS attacks
Dolibarr released updated versions to counter the SQL Injection/ XSS attacks which are present in the versions lower than 3.5.3.

### Evidence 2: User Database Verification
Dolibarr performs the user data verification so that any attempts to make a false payment to trigger the SQL/XSS Injection can be avoided by allowing only legit users to make donations.

### Evidence 3: Dolibarr Security Documentation about SSL and TLS
Dolibarr security document states that updated certificates of TLS and SSL are used to counter the attacks made by hackers to intercept transactions.

### Evidence 4: Card payment logs report
Dolibarr uses cross match payment method to verify the transactions with the help of card payment log reports.



## References:
* https://securityintelligence.com/posts/how-to-prevent-http-parameter-pollution/
* https://security.snyk.io/vuln/SNYK-PHP-DOLIBARRDOLIBARR-560379
* https://wiki.dolibarr.org/index.php?title=Security_information#Features


## Planning and Reflection:  
This time initially we had some confusion in building assurance cases from the scratch but managed to do by brainstorming number of ideas and went with a good plan. We connected twice in a week and even more times whenever there is a dependency or needed any help from other team mates. We divided the tasks to build the assurance case diagrams before meeting the instructor check-in meeting and drafted some of our ideas. We took the feedback from instructor which made us think to involve more doubts in to the picture so that it makes more sense. Everyone has worked hard to complete this task on time.

## Project Board

<<<<<<< HEAD
[GitHub Project Board](https://github.com/users/SreeharshaMorampudi/projects/3)
=======
[GitHub Project Board]()

>>>>>>> 21ad8d06139d1557e8455cb84785333222e4f204
