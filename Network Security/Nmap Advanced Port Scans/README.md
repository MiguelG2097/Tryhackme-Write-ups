# Task1 - Introduction

No answer needed

# Task 2 - TCP Null Scan, FIN Scan, and Xmas Scan 


In a null scan, how many flags are set to 1?

R/ 0


In a FIN scan, how many flags are set to 1?

R/ 1


In a Xmas scan, how many flags are set to 1?

R/ 3


Start the VM and load the AttackBox. Once both are ready, open the terminal on the AttackBox and use nmap to launch a FIN scan against the target VM. How many ports appear as open|filtered?

We will need to lunch a port scan against the try hack me machine. To run the FIN scan we will use the command: **nmap -sF TRYHACKME IP MACHINE**. As result we will get 7 ports as open|filtered.

R/ 7


Repeat your scan launching a null scan against the target VM. How many ports appear as open|filtered?

We will need to lunch a port scan against the try hack me machine. To run the NULL scan we will use the command: **nmap -sN TRYHACKME IP MACHINE**. As result we will get 7 ports as open|filtered.

R/ 7

# Task 3 - TCP Maimon Scan 

R/ 2
