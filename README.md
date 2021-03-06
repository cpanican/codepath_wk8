# Project 8 - Pentesting Live Targets

Time spent: **4** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection (SQLi)
![](./gifs/1.gif)

Instead of an ID number, the attacker enters this command `' OR SLEEP(5)=0--'`. Notice how it took around 5 seconds for website to query the data.

Vulnerability #2: Session Hijacking/Fixation
![](./gifs/2.gif)

The attacker can log in from the site by using a session ID.


## Green

Vulnerability #1: Username Enumeration
![](./gifs/3.gif)

Notice that the error message is bolded if username exists. The error message is in plain text if username does not exist. 

Vulnerability #2: Cross-Site Scripting (XSS)
![](./gifs/4.gif)

## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
![](./gifs/5.gif)

Attacker can access information that is not usually available to the public by changing the `id` parameter.

Vulnerability #2: Cross-Site Request Forgery (CSRF)
![](./gifs/6.gif)

User can update the database even after changing the CSRF token.


## Notes

Describe any challenges encountered while doing the work:

1. For Green#2, viewing the contact page responses is shared by other students. So, their scripts also will trigger.
