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
