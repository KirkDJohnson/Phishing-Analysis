<h1>Malicious Phishing Analysis Lab (Incomplete)</h1>


<h2>Description</h2>
TEXT
<br />
<h2>Utilities Used</h2>

- <b>Phishtool</b> 
- <b>VirusTotal</b>
- <b>any.run</b>
- <b>Talos Intelligence</b>
- <b>URL2PNG</b>
- <b>Talos Intelligence</b>


<h2>Environments Used </h2>

- <b>Windows 10</b> 
- <b>Kali Linux</b> 
<h2>Lab Overview:</h2>

<p align="center">
First opened the email in thunderbird mail to see it as the reciever would first see the email for a baseline.<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/09861a53-26a7-4811-99ab-39306c7b8355"  alt="Phishing Analysis"/>
<br />
<br />
Upon reading through the contents of the email this phrase was an immedaite red flag as an excuse for recieving an email from a non-recognized sender and establish trust.<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/2cb37b20-d467-4831-a70f-a5093a402a53"  alt="Phishing Analysis"/>
<br />
<br />
In a safe sanboxed enviornment I downloaded the attachment from the email and obtained the sha256 hash value through the terminal <br/>
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
Lastly, I checked any.run which contains samples and greater detailed reports about malware where it was uncovered the type of malware that the attachment was: Agent Tesla<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/981cba13-cba7-4196-a931-5d48c63736b7"  alt="Phishing Analysis"/>
<br />
<br />
TEXT<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/e2b92b11-f412-465b-b6bf-6040ec87342c"  alt="Phishing Analysis"/>
<br />
<br />
TEXT<br/>
<img src=""  alt="Phishing Analysis"/>
<br />
<br />
TEXT<br/>
<img src="https://github.com/KirkDJohnson/Phishing-Analysis/assets/164972007/fe77a94b-bb87-4f1b-a898-03576f453f39"  alt="Phishing Analysis"/>
<br />
<br />

<h2>Thoughts</h2>
TEXT
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
