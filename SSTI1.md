# SSTI1

**Author:** Venax

## Description

I made a cool website where you can announce whatever you want! Try it out!

I heard templating is a cool and modular way to build web apps! Check out my website here!

**Hints:** Server Side Template Injection

# SSTI1

**Author:** Venax

## Description

I made a cool website where you can announce whatever you want! Try it out!

I heard templating is a cool and modular way to build web apps! Check out my website here!

**Hints:** Server Side Template Injection

## What is SSTI?

Server Side Template Injection (SSTI) is a vulnerability that occurs when user input is embedded into a template engine in an unsafe way. Instead of treating the input as plain text, the server **executes it as code**, which can allow an attacker to:

- Read sensitive files on the server
- Execute arbitrary commands
- Gain full control of the server in some cases

Common template engines vulnerable to SSTI include **Jinja2** (Python), **Twig** (PHP), and **Freemarker** (Java).

## Solution

![steps](Images/SSTI.png)

Detect SSTI vulnerability potential.
The payload I used to Identify if there is SSTI vulnerability potential is {{7*7}}

Identify The Terminal Engine:
![steps](Images/SSTI1.png)
1.I started at {{7*7}} ouputs 49
![steps](Images/1.png) ![steps](Images/2.png)
2.then {{7*'7'}} outputs 49
3.then I choose Jinja2

I read about Jinja2 syntax and since I never have done this before used Claude to better underderstand and get the syntax I needed

Here's the syntax in order with explanation

Sources:
https://hacktricks.wiki/en/pentesting-web/ssti-server-side-template-injection/jinja2-ssti.html

https://portswigger.net/web-security/server-side-template-injection#constructing-a-server-side-template-injection-attack

## Flag

(put the flag here)
