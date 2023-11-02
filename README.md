# Cybersecurity Incident Report for yummyrecipesforme: Applying OS Hardening Techniques

---

While working as a cybersecurity analyst for yummyrecipesforme.com, a (**fictional**) website that sells recipes and cookbooks. A disgruntled baker decided to publish the website’s best-selling recipes on their website for the public to access for free. 

The baker executed a dictionary attack; a type of brute force attack to gain access to the web host. Later investigations reveal they repeatedly entered several known default passwords for the administrative account until they entered the correct password. After obtaining the login credentials, the malicious actor was able to access the admin panel and change our website’s source code. Investigations reveal they embedded a JavaScript function in the website's source code that prompted visitors to download and run a file upon visiting the website. After executing the file, the victims are redirected to a fake version of our website where our recipes are now available for free.

We were made aware of the incident multiple customers emailed yummyrecipesforme’s helpdesk. These customers complained that the company’s website had prompted them to download a file to update their browsers. They claimed that, after running the file, the address of the website changed and their personal systems began running slower. When responding to this incident, the website owner attempted to log in to the web host's admin panel but was unable to due to the credentials being changed. They then reached out to the website hosting provider. I and other cybersecurity analysts were then tasked with investigating this security event.

To address the incident, I created a sandbox environment to observe the suspicious website behavior. Then I ran the network protocol analyzer, tcpdump, before visiting the website, yummyrecipesforme.com. Once the website loaded, I was prompted to download an suspicious executable file to update my browser. Investigating further, I accepted the download and executed the file. Once executed, I observed that my browser redirected me to a different URL, greatrecipesforme.com, which was designed to appear like our website, yummyrecipesforme.com. However, the recipes our company sells were posted for free on this website. 

A senior cybersecurity professional's analysis confirms that the website was compromised. The analyst checked the website's sourcecode and noticed that JavaScript code had been added to prompt our website's visitors to download an executable file. Analysis of the downloaded file found a script that redirects the visitors’ browsers from yummyrecipesforme.com to greatrecipesforme.com. 

The cybersecurity team reports that the web server was impacted by a brute force attack. The disgruntled baker was able to guess the password easily because the admin password was still set to the default password. Additionally, there were no controls in place to prevent a brute force attack. 

Your job is to document the incident in detail, including identifying the network protocols used to establish the connection between the user and the website.  You should also recommend a security action to take to prevent brute force attacks in the future.



---
