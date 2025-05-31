---
title: Unprotected admin functionality with unpredictable URL
author: Gamezilla
date: 2025-05-30 14:00:00 +0100
categories: [PortSwigger]
comments: false
toc: false
pin: false
tags: [portswigger, burp, burpsuite, SSV, courses, UAFWUURL]
math: false
mermaid: false
---

## 1. Statement

This lab has an unprotected admin panel. It's located at an unpredictable location, but the location is disclosed somewhere in the application.

Solve the lab by accessing the admin panel, and using it to delete the user carlos.

![enonce](/assets/img/posts/PortSwigger/ServerSideVulnerabilities/UAFWUURL/enonce.png)


---

## 2. Challenge

### a. Unprotected Admin Functionality With Unpredictable URL, what is it ?

In some cases, sensitive functionality is concealed by giving it a less predictable URL. This is an example of so-called "security by obscurity". However, hiding sensitive functionality does not provide effective access control because users might discover the obfuscated URL in a number of ways.

Imagine an application that hosts administrative functions at the following URL:

https://insecure-website.com/administrator-panel-yb556

This might not be directly guessable by an attacker. However, the application might still leak the URL to users. The URL might be disclosed in JavaScript that constructs the user interface based on the user's role:

```java
<script>
	var isAdmin = false;
	if (isAdmin) {
		...
		var adminPanelTag = document.createElement('a');
		adminPanelTag.setAttribute('href', 'https://insecure-website.com/administrator-panel-yb556');
		adminPanelTag.innerText = 'Admin panel';
		...
	}
</script>
```
This script adds a link to the user's UI if they are an admin user. However, the script containing the URL is visible to all users regardless of their role.
---

### b. Vulnerability Analysis

As the course explains it to us, as we arrive on the website, we want to try to search for the Developer Mode of our preferred browser :


![console](/assets/img/posts/PortSwigger/ServerSideVulnerabilities/UAFWUURL/console.png)

```java
var isAdmin = false;
if (isAdmin) {
   var topLinksTag = document.getElementsByClassName("top-links")[0];
   var adminPanelTag = document.createElement('a');
   adminPanelTag.setAttribute('href', '/admin-fvas19');
   adminPanelTag.innerText = 'Admin panel';
   topLinksTag.append(adminPanelTag);
   var pTag = document.createElement('p');
   pTag.innerText = '|';
   topLinksTag.appendChild(pTag);
```

We then want to see what is the administrator-panel about : 

https://lab-website.com/admin-fvas19

As we find the administrator panel, we can, now, delete the "Carlos" user just by pressing the Delete button next to his name and that ends the challenge, and hereby the writeup

![ending](/assets/img/posts/PortSwigger/ServerSideVulnerabilities/UAFWUURL/ending.png)

---

## END of the writeup.

