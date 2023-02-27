# Task 1 - Introduction

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

# Task 4 - TCP ACK, Window, and Custom Scan 

In TCP Window scan, how many flags are set? 

R/ 1

You decided to experiment with a custom TCP scan that has the reset flag set. What would you add after --scanflags? 

R/ RST


The VM received an update to its firewall ruleset. A new port is now allowed by the firewall. After you make sure that you have terminated the VM from Task 2, start the VM for this task. Launch the AttackBox if you haven't done that already. Once both are ready, open the terminal on the AttackBox and use Nmap to launch an ACK scan against the target VM. How many ports appear unfiltered?

R/ 4


What is the new port number that appeared?

R/ 443


Is there any service behind the newly discovered port number? (Y/N)

R/ N
