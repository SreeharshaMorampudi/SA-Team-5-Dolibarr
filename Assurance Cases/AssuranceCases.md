# Assurance Cases for Software Security Engineering  

## Assurance Case 1:
![Assurance Case 1 Diagram](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Assurance%20Cases/AssuranceCase%20Diagram1%20(2).jpg)


### Evidence 1: Usage of CAPTCHA
The usage of CAPTCHA in Dolibarr makes it difficult for hackers to perform multiple login attempts using random passwords.  

### Evidence 2: Log Report of multiple unsuccessful attempts and block the IP address
Dolibarr allows Admin to block the IP addresses he found suspicious with multiple unsuccessful login attempts.  

### Evidence 3: Time based OTP
Using Two-Factor Authentication, Dolibarr sends a One Time Password to be entered by the user so that even if Hacker knows the login details he cannot log in to the system.  

### Evidence 4: Strong Password Policy
Dolibarr has rules to make strong passwords for the users so that users need not worry about dictionary attacks.  

### Evidence 5: Strong Password Management policy
In Dolibarr Admin can refresh the user's password anytime or from time to time so that even if the passwords are leaked in a data breach, Hackers can be prevented from login into the system.  


## Assurance Case 2:
![Assurance Case 2 Diagram](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Assurance%20Cases/Assurance%20Case%20Diagram%202.2.jpg)

### Evidence 1: Docusign Security Feature
By implementing DocuSign Module in Dolibarr, the documents can be shared only with the intended users so that no modifications or false confirmations can be avoided by hackers.

### Evidence 2: Log Report on File modifications
As the files shared will be read-only, any attempts of changes in the files can be found using the log report on file modifications.  

### Evidence 3: Man in the middle report
As files are shared using links, All communications to and from Dolibarr are secured because TLS/SSL is used.  


## Assurance Case 3:
![Assurance Case 3 Diagram](https://github.com/SreeharshaMorampudi/SA-Team-5-Dolibarr/blob/main/Assurance%20Cases/Assurance%20Case%20Diagram%203.3.jpg)

### Evidence 1: Counter SQL Injection/XSS attacks
Dolibarr released updated versions to counter the SQL Injection/ XSS attacks in versions lower than 3.5.3.

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
This time initially we had some confusion in building assurance cases from the scratch but managed to do by brainstorming a number of ideas and going with a good plan. We connected twice a week and even more times whenever there was a dependency or needed help from other teammates. We divided the tasks to build the assurance case diagrams before meeting the instructor check-in meeting and drafted some of our ideas. We took the feedback from the instructor which made us think to involve more doubts into the picture so that it makes more sense. Everyone has worked hard to complete this task on time.

## Project Board:
[GitHub Project Board]()
