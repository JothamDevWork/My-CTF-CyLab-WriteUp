# SSTI1

**Author:** Venax

## Description

I made a cool website where you can announce whatever you want! Try it out!

I heard templating is a cool and modular way to build web apps! Check out my website here!

**Hints:** Server Side Template Injection

## What is SSTI?

Server Side Template Injection (SSTI) is a vulnerability that occurs when user input
is embedded into a template engine in an unsafe way. Instead of treating the input as
plain text, the server **executes it as code**, which can allow an attacker to:

- Read sensitive files on the server
- Execute arbitrary commands
- Gain full control of the server in some cases

Common template engines vulnerable to SSTI include **Jinja2** (Python),
**Twig** (PHP), and **Freemarker** (Java).

## Solution

### Step 1: Detect SSTI Vulnerability

![steps](Images/SSTI.png)

The payload I used to identify if there is an SSTI vulnerability is `{{7*7}}`

### Step 2: Identify the Template Engine

![steps](Images/SSTI1.png)

1. `{{7*7}}` outputs `49`

![steps](Images/1.png)
![steps](Images/2.png)

2. `{{7*'7'}}` outputs `49`
3. Based on the results, I identified the template engine as **Jinja2**

### Step 3: Exploit with Jinja2

(add your payloads and explanation here)

## Sources

- [HackTricks - Jinja2 SSTI](https://hacktricks.wiki/en/pentesting-web/ssti-server-side-template-injection/jinja2-ssti.html)
- [PortSwigger - SSTI](https://portswigger.net/web-security/server-side-template-injection#constructing-a-server-side-template-injection-attack)

## Flag

(put the flag here)
