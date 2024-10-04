# SQL Injection(Login Form)

Name: Rory Stiff 

Date: July 24, 2024

Disclaimer: This is for educational purposes only.

SQL Injection

In this section, I will explain what SQL injection is, describe some common examples, explain how to find and
exploit various kinds of SQL injection vulnarabilities, and show you how to prevent SQL injections.

what is an SQL Injection?

SQL injection is a vulnarability that allows an attacker to interfere and disrupt queries within a database.
This usally alllows the attacker to veiw data they normally would not be able to see. This data that the
attacker can see now is compromised because they can now make changes to the application that can disrupt the 
applications behavior.


![image](https://github.com/user-attachments/assets/b231c557-c130-4453-9493-9628eb23981b)



Example Description: 

In this example I will be showing you how an SQL injection works and showing you how to
use a SQL.txt file to attack a web application Login page. As you can see down below there are two
application images the foxy proxy applications allows me to listen to the port of the web server and be able to 
see the traffic from there. Burpsuite is an application that works with foxy proxy that allows us to see the web tarffic
within the web browser. I am using OWASP(Open WEb Application secuirty Project) for this example. On the site
there is a vulnarable web application wich is bWAPP. That will be where I am showing how to do this.

Here are links for setting up virtual box and the 2 application(burpsuite, foxy proxy)...

https://www.youtube.com/watch?v=jHGNLvSpaLs

https://www.youtube.com/watch?v=pfaa9YDypJc&t=315s

https://www.youtube.com/watch?v=sBzL_zoYt6o





![image](https://github.com/user-attachments/assets/cbdcad07-4f92-4c95-aa0a-59cfaeb4f5c3)





![image](https://github.com/user-attachments/assets/9e6f93ad-f3c5-4000-8540-6aca63e8f6ae)


![image](https://github.com/user-attachments/assets/7f323317-8270-4101-ba43-dc3ee530d0e3)







SQL Injection Example:


Step 1. 


Create an account with bWAPP then click the tab that says choose your bug. After doing that clcick on
the tab that says SQL Injection(Login Form). 


![image](https://github.com/user-attachments/assets/c0088d2f-ee44-41e2-8bb0-f800bd1a93fc)




Step 2. 

Open up burpsuite and head over to the tab where it says proxy. After doing that there should be a tab that says 
interception on. What this dose is it allows the application to listen to the foxy proxy running on google or firefox. You will also
want to head over to the top of your web page and turn of on the foxy proxy.





![image](https://github.com/user-attachments/assets/78c43152-5117-442b-a3ca-401fbf9564a2)



![image](https://github.com/user-attachments/assets/df8758eb-03e1-4d0b-baf0-1f9899a31b64)







Step 3.


Next we need to send this to the intruder so we can clear the payloads. Then we need to add a payload wich we will
highlight the login field and hit the add button wich adds the payload. 




![image](https://github.com/user-attachments/assets/e5b2eebd-80bc-4838-9652-5c52727b0f34)





tip: first just hit the clear button then hit highlight the login field then hit add.




![image](https://github.com/user-attachments/assets/1fc383ff-5165-4cf0-aeee-8d61a9830141)







Step 4. 



For this step we will need to have an SQL.txt that has a list of common SQL commands for attacking web applications. 
Aftering obtaining the SQL.txt file we can head over back to burpsuite and go to the payloads tab. Once you are there head to
where it says add a simple list. Add the SQL.txt file you had then hit start attack in the top right corner of the web application.




![image](https://github.com/user-attachments/assets/f879d557-7564-4dfd-8952-f5e822dddea5)





Now hit start attack...






Step 5.


Now that you have started the attack it will try to find the SQL commands that work. If you click one of the commands and head over to 
the response tabe and click the render tab it should show you something like this saying if it was a success or not.




![image](https://github.com/user-attachments/assets/1a401a75-deac-4614-8fdb-02058ffd4da3)






summary of what we just did:


Using Burpsuite and froxy proxy we succussfully gain access to a data we are not supposed to have. We conducted an SQL injection in bWAPP
on a Login Form page and showed how we can use these applications to test and to see if the web page is vulnarble to SQL Injection Attacks.





How to prevent SQL Injections:


step 1. Validate input



step 2. Prepared querries


step 3. cretae prepared staments


step 4. Bind the parameters


step 5. Execute Query


step 6. Fetch result































