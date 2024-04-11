<h1>Malicious Phishing Analysis Lab</h1>


<h2>Description</h2>
In this lab, I gained hands-on experience examining a phishing email with a malicious attachment. While there are multiple ways to handle phishing emails depending on the playbook of the company, I conducted due diligence on the email sender and the malicious attachment. I began by opening the email in Thunderbird mail to get a clear view of how the user saw the email and immediately noticed phishing language tactics to establish trust and excuse the unknown sender's email name. I then uploaded the email into Phishtool, an all-in-one tool to help extract useful fields from emails and determine the authenticity of the email. After conducting some research on the sender's domain and IP and coming up empty, I shifted my focus to the attachment. I safely downloaded the attachment and immediately obtained its hash, then began using threat intelligence resources. It quickly became clear that the attachment was malicious, containing the malware Agent Tesla, which is a popular trojan/spyware. Lastly, I found a Sigma rule that can be used in many instances to block the sender and detect if the indicator of compormise is present in the future.
<br />
<h2>Utilities Used</h2>

- <b>Phishtool</b> 
- <b>VirusTotal</b>
- <b>any.run</b>
- <b>Talos Intelligence</b>
- <b>URL2PNG</b>
- <b>AbuseIPDB</b>


<h2>Environments Used </h2>

- <b>Windows 10</b> 
- <b>Kali Linux</b> 
<h2>Lab Overview:</h2>

<p align="center">
First, I opened the email in thunderbird mail to see it as the reciever would first see the email for a baseline.<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/09861a53-26a7-4811-99ab-39306c7b8355"  alt="Phishing Analysis"/>
<br />
<br />
Upon reading through the contents of the email this phrase was an immedaite red flag as an excuse for recieving an email from a non-recognized sender and establish trust.<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/2cb37b20-d467-4831-a70f-a5093a402a53"  alt="Phishing Analysis"/>
<br />
<br />
To begin deeper analysis on the email, I uploaded it to Phishtool to extract important elements such as header details (originating IP, return-patch, etc) and security checks<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/934ffc37-1350-4938-afb8-069775d09376"  alt="Phishing Analysis"/>
<br />
<br /> 
Seeing that SPF failed is an indicator that the email was likely spoofed and the domain did not approve the IP of the sender<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/dd103df2-0747-479f-9bff-9fc2223163ad"  alt="Phishing Analysis"/>
<br />
<br /> 
Looking into the sender's IP, it appeared to be clean through all resources with it originating from Canada<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/fe77a94b-bb87-4f1b-a898-03576f453f39"  alt="Phishing Analysis"/>
<br />
<br />
Lastly, for the email analysis, I safely examined the domain/website of the attacker through URL2PNG and it is clear the website did match the the information in the email, however I thought it was suspicious by the design and style of the website<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/69a5544a-b12c-42a9-b691-4ad56390e881"  alt="Phishing Analysis"/>
<br />
<br /> 
In a safe sanboxed environment I downloaded the attachment from the email and obtained the sha256 hash value through the terminal <br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/874820ef-c1e5-4a75-91ba-71ca5d57f270"  alt="Phishing Analysis"/>
<br />
<br />
With the hash, I input it into mulitple threat intelligence resources and found considerable evidence of it to be malicious<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/0635ea6c-c16b-4bd9-967f-d7d8fdcf2049"  alt="Phishing Analysis"/>
<br />
<br />
Same hash uploaded to virustotal to get a second answer and learn more about it<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/6ad43c5d-a161-447f-99c8-cf1f9fc4c99e"  alt="Phishing Analysis"/>
<br />
<br />
 I checked any.run which contains samples and greater detailed reports about malware where it was uncovered the type of malware that the attachment was: Agent Tesla<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/981cba13-cba7-4196-a931-5d48c63736b7"  alt="Phishing Analysis"/>
<br />
<br />
Researching more into Agent Tesla, it is one of the most common malware currently depsite being around for a decade  <br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/e2b92b11-f412-465b-b6bf-6040ec87342c"  alt="Phishing Analysis"/>
<br />
<br />
;astly, to further reduce the chance of the malware infecting a host if come accross in the future, I found a Sigma rule to detect the presence of Agent Tesla IOC to add to the defence of blocking the hash, IP, and domain of attacker<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/9b966f9f-0fb2-4c04-adf0-f2c717b62809"  alt="Phishing Analysis"/>
<br />
<br />

<h2>Thoughts</h2>
This lab was incredibly enjoyable as it provided me with hands-on experience in analyzing a phishing email. I learned to identify subtle elements and social engineering techniques commonly employed by attackers in phishing attempts. Additionally, safely handling live malware, utilizing threat intelligence, and identifying it as a pervasive and dangerous sample like Agent Tesla was particularly intriguing. Examining how the malware behaves in platforms like any.run to pinpoint indicators of compromise (IOCs) was also a valuable learning experience gained from this lab. Now, I would feel  more confident in handling a phishing alert ticket in a live environment. Lastly, I've become more familiar with various open-source tools that can aid in analyzing emails and assessing potential attachments or embedded links.
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
