<h1 align="center">Analysis of HTTP Traffic</h1>
<h2>Description</h2>
This Project was centered around the security of HTTP vs HTTPS websites with a focus on identifying websites with a lack of security. To emulate a MITM attack, I used an Attack VM running Kali Linux, and a Victim VM running Ubuntu. I used Wireshark to scan the packets being sent by the Victim VM and examining the content to see if any data leaks from these websites.
<br/>
<br/>

<h2>Baseline Test</h2>
This is a screenshot of one of the packets being sent from Google. Google use HTTPS which employs TLS for their encryption and as you can see, it is effective.
<br/>
<br/>
<br/>
<br/>

![image](https://github.com/user-attachments/assets/935d0073-afe3-4df2-b0c0-95b4166b3b7b)

<h2>List of Sites Tested</h2>
I would not recommend anyone visiting these sites. They are very insecure and possibly dangerous. These are the sites that I used for the analysis <br/><br/>
-http://www.Baidu.com<br/>
-http://swiat-kamienia.pl<br/>
-http://www.shippingchina.com/office/login/index.html<br/>
-http://www.360doc.com/index.html<br/>
<br/>
<br/>

<h2>Results of Traffic Analysis</h2>
<b>"Baidu"</b>
<br/>
<br/>

![image](https://github.com/user-attachments/assets/f6a30a9d-988d-4bdf-b86e-daca52aeb3ff)


Baidu was a bit of a concern. The username was being sent in plaintext in the HTTP packet. I don't believe the password was sent as plaintext as it would have appeared in my search.<br/>
This is still a very insecure network, and I would advise staying away.
<br/>
<br/>
<b>"Swiat-Kamienia"</b>
<br/>
<br/>

![image](https://github.com/user-attachments/assets/d56b3f12-2eb2-45a0-84ce-c39aabb6a5bb)

Swiat-kamienia was an absolute fail. Clearly sent username and password as cleartext in the packet.<br/>
This is a cybersecurity hazard. A good example of why we should use HTTPS websites.
<br/>
<br/>
<b>"Shippingchina.com"</b>
<br/>
<br/>

![image](https://github.com/user-attachments/assets/36c3dc37-51f4-4699-b669-ef998a892456)

Shippingchina is another fail. This website was sending in plaintext as well.<br/>
<br/>
<b>"360Doc"</b>
<br/>
<br/>

![image](https://github.com/user-attachments/assets/e127a24f-beab-4493-a0a9-7a28b963fc2a)

360Doc was partially secure. The email was not secured, at least the password wasn't sent as plaintext on this website.<br/>
<br/>
<h2>Conclusion</h2>
These site are all insecure and could be potentially harmful to you. In the event of a MITM attack, your data would be compromised. 
Luckily, 81% of websites use HTTPS today, and the ones I found that still use insecure HTTP are fairly rare.
Ultimately, this is a somewhat archaic analysis as its not the industry standard anymore, but is a good look into encryption.
