## Affected Plugin
* WP Booking Calendar
* Exploit Title: WP Booking Calendar has multiple  cross-site scripting vulnerabilities
* Active installations50,000+
* Vendor Homepage:https://wordpress.org/plugins/booking
* Software Link: https://wordpress.org/plugins/booking
* Version: 10.5.1   
* Proof of Concept:
## Part one：First vulnerability
1. Create an author account
![images](https://github.com/BigTiger2020/2024/blob/main/1.png)
2. Log in with author account
![images](https://github.com/BigTiger2020/2024/blob/main/2.png)
3. Insert attack statement:'-prompt(1)-'
![images](https://github.com/BigTiger2020/2024/blob/main/3.png)
4. Successful execution of attack statement
![images](https://github.com/BigTiger2020/2024/blob/main/4.png)
5. Log in to the database to check that the attack statement was successfully saved to the database.
![images](https://github.com/BigTiger2020/2024/blob/main/5.png)
6. Therefore, this vulnerability is a stored cross-site scripting vulnerability.
## Part two：Second vulnerability
1. Also use the author account to insert attack statements:'-prompt(1)-'
![images](https://github.com/BigTiger2020/2024/blob/main/6.png)
2. Successful execution of attack statement
![images](https://github.com/BigTiger2020/2024/blob/main/7.png)
3. Log in to the database to check that the attack statement was successfully saved to the database.
![images](https://github.com/BigTiger2020/2024/blob/main/8.png)
4. Therefore, this vulnerability is a stored cross-site scripting vulnerability.
## Part three：The third vulnerability
1. Also use the author account to insert attack statements: prompt(1)
![images](https://github.com/BigTiger2020/2024/blob/main/9.png)
2. Successful execution of attack statement
![images](https://github.com/BigTiger2020/2024/blob/main/10.png)
3. Check the database, the attack statement is not stored in the database
![images](https://github.com/BigTiger2020/2024/blob/main/11.png)
4. Therefore, this vulnerability is a reflected cross-site scripting vulnerability.
## Summarize
In summary, there are three cross-site scripting attack vulnerabilities in the WP Booking Calendar plug-in, two of which are stored cross-site scripting attack vulnerabilities and one is a reflected cross-site scripting attack vulnerability.
