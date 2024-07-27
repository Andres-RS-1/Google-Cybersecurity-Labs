Analyze the following case. Then, complete the instructions step by step.

You are a cybersecurity analyst for yummyrecipesforme.com, a website that sells recipes and cookbooks. A disgruntled baker has decided to publish the website's best-selling recipes so that the public can access them for free.

The baker executed a brute force attack to access the web host. He repeatedly entered several known default passwords for the administrative account until he hit on the correct one. After obtaining the access credentials, he was able to access the administration panel and modify the website's source code. She embedded a JavaScript function in the source code that asked visitors to download and run a file when visiting the website. After running the downloaded file, customers were redirected to a fake version of the website where the seller's recipes were already available for free.

Several hours after the attack, several customers sent emails to yummyrecipesforme support. They complained that the company's website had asked them to download a file to update their browsers. Customers reported that after running the file, the website address changed and their personal computers started running slower.

In response to this incident, the website owner tries to log in to the admin panel but is unsuccessful, so he contacts the website's hosting provider. You and other cybersecurity analysts are tasked with investigating this security incident.

To address it, you create a sandbox environment to observe suspicious website behavior. Run the tcpdump network protocol analyzer and type the website URL, yummyrecipesforme.com. As soon as the website loads, you are asked to download an executable file to update your browser. You accept the download and allow the file to run. Then you notice that your browser redirects you to a different URL, greatrecipesforme.com, which is designed to look like the original site. However, the recipes your business sells are now published for free on the new website.

The logs show the following process:

The browser requests a DNS resolution of the URL yummyrecipesforme.com.

The DNS server responds with the correct IP address.

The browser initiates an HTTP request for the web page.

The browser starts downloading the malware.

The browser requests another DNS resolution for greatrecipesforme.com.

The DNS server responds with the new IP address.

The browser initiates an HTTP request to the new IP address.

A senior analyst confirms that the website was compromised. The analyst verifies the source code of the website. He notes that JavaScript code has been added to prompt website visitors to download an executable file. Analysis of the downloaded file found a script that redirects the browsers of visitors from yummyrecipesforme.com to greatrecipesforme.com.

The cybersecurity team reports that the web server was affected by a brute force attack. The disgruntled baker was able to guess the password easily because the administrator password was still the default password. Additionally, there were no controls to prevent a brute force attack.

Your job is to document the incident in detail, including identifying the network protocols used to establish the connection between the user and the website. You should also recommend a security action to take to prevent brute force attacks in the future.
