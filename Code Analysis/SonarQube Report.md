
# 1. CWE-295: Improper Certificate Validation

### Change this code to use a stronger protocol
![image](https://user-images.githubusercontent.com/100978590/205523906-aa82a31e-0f54-4a06-88e1-8d1cfc605f47.png)  
![image](https://user-images.githubusercontent.com/100978590/205523999-05a7c1be-e229-4cdc-971c-6e2901b170d2.png)

Solution: Force the user to use the latest version. Force the user to makesure to use HTTPS.
dolibarr-develop/htdocs/includes/swiftmailer/lib/classes/Swift/Transport/StreamBuffer.php

### Enable server certificate validation on this SSL/TLS connection
![image](https://user-images.githubusercontent.com/100978590/205523685-5be16003-c1d1-4f5f-81ca-a2be800ad474.png)  
dolibarr-develop/htdocs/includes/restler/framework/Luracast/Restler/Resources.php  
Solution: Should be made as TRUE and Force the browser to check verify the TLS cert.

### Enable server certificate validation on this SSL/TLS connection
![image](https://user-images.githubusercontent.com/100978590/205524032-e09010d5-4c0a-4048-b89a-c9a4afad2110.png)  
dolibarr-develop/htdocs/includes/tecnickcom/tcpdf/include/tcpdf_static.php  
Solution: Should be made as TRUE and Force the browser to check verify the TLS cert.

### Enable server certificate validation on this SSL/TLS connection
![image](https://user-images.githubusercontent.com/100978590/205524105-0040f4ca-e920-4e5b-b358-3a0c025b8179.png)  
dolibarr-develop/htdocs/includes/tecnickcom/tcpdf/include/tcpdf_static.php  
Solution: Should be made as TRUE and Force the browser to check verify the TLS cert.


# 2. CWE-327: Use of a Broken or Risky Cryptographic Algorithm  
### Use a strong cipher algorithm  
![image](https://user-images.githubusercontent.com/100978590/205524224-cf3b9d45-2009-4f06-be1e-0f8871e552d9.png)  
dolibarr-develop/htdocs/includes/swiftmailer/lib/classes/Swift/Transport/Esmtp/Auth/NTLMAuthenticator.php  
Sol: DES is an outdated Cipher algorithm, we should use AES instead of DES.
### Use secure mode and padding scheme
![image](https://user-images.githubusercontent.com/100978590/205524310-2ca38381-9fb7-4062-8346-c23530222ed1.png)
dolibarr-develop/htdocs/includes/swiftmailer/lib/classes/Swift/Transport/Esmtp/Auth/NTLMAuthenticator.php  
### Change this code to use a stronger protocol
![image](https://user-images.githubusercontent.com/100978590/205524343-24fe06a7-7c71-42b3-8b45-ee71670c082c.png)
![image](https://user-images.githubusercontent.com/100978590/205524396-2f318e29-7c08-4864-88c3-c6453c8b3427.png)

dolibarr-develop/htdocs/includes/swiftmailer/lib/classes/Swift/Transport/StreamBuffer.php  

# 3. CWE-326: Inadequate Encryption Strength

### Use Strong Cipher algorithm
![image](https://user-images.githubusercontent.com/100978590/205524530-c5bda5c3-c2fd-4d31-90b5-68b80c91ac38.png)
dolibarr-develop/htdocs/includes/swiftmailer/lib/classes/Swift/Transport/Esmtp/Auth/NTLMAuthenticator.php

### Change this code to use a stronger protocol
![image](https://user-images.githubusercontent.com/100978590/205524564-ce248bcb-f3f9-4680-acad-8a33f0ba31e3.png)
dolibarr-develop/htdocs/includes/swiftmailer/lib/classes/Swift/Transport/StreamBuffer.php  
### Change this code to use a stronger protocol
![image](https://user-images.githubusercontent.com/100978590/205524589-15304f35-a388-43f7-9798-673fdb2dc2a2.png)

# 4. CWE-297: Improper Validation of Certificate with Host Mismatch
### Enable server hostname verification on this SSL/TLS connection
![image](https://user-images.githubusercontent.com/100978590/205524645-93aeb87a-7267-46ef-92c3-d55ab6ff8198.png)
dolibarr-develop/htdocs/includes/tecnickcom/tcpdf/include/tcpdf_static.php

### Enable server hostname verification on this SSL/TLS connection
![image](https://user-images.githubusercontent.com/100978590/205524686-42be2671-71b4-46fe-8dd8-2bf6de2c5603.png)
dolibarr-develop/htdocs/includes/tecnickcom/tcpdf/include/tcpdf_static.php
Solution: Make it as TRUE to verify if the HostName is not the malicious one.

# 5. CWE-521: Weak Password Requirements
### Provide username and password to authenticate the connection
![image](https://user-images.githubusercontent.com/100978590/205524768-8adfe4c9-8111-4447-acf4-6fc20fc56fd6.png)
dolibarr-develop/htdocs/core/class/ldap.class.php
Sol: Check if the user is logged in to authenticate this page.

# 6. CWE-611: Improper Restriction of XML External Entity Reference  
### Disable access to external entities in XML parsing
![image](https://user-images.githubusercontent.com/100978590/205524823-d125f515-05f5-4483-bb23-3d62ef67386c.png)
dolibarr-develop/htdocs/includes/symfony/var-dumper/Tests/Caster/XmlReaderCasterTest.php  
prob: Reading the XML files without sanitization, which the attacker could include malicious external entities that may cause the command injections.
Sol: Do some sanitization to avoid external entities in XML(XXE) Parsing.


# 7. CWE-780: Use of RSA Algorithm without OAEP
### Use secure mode and padding scheme
![image](https://user-images.githubusercontent.com/100978590/205524893-e367137c-dd14-43dd-a799-3485f53ae5e1.png)
dolibarr-develop/htdocs/includes/swiftmailer/lib/classes/Swift/Transport/Esmtp/Auth/NTLMAuthenticator.php

# 8. CWE-827: Improper Control of Document Type Definition
### Disable access to external entities in XML parsing  
![image](https://user-images.githubusercontent.com/100978590/205524975-25ecfd00-9679-4b6b-8a0f-83b0f392cd8b.png)  
dolibarr-develop/htdocs/includes/symfony/var-dumper/Tests/Caster/XmlReaderCasterTest.php
