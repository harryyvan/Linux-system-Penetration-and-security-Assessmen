<h1>Linux system Penetration and security Assessment(Tryhackme)</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
My project consiste of engaging in a control environmennt using Tryhackme attackbox to understand the process of accessing and securing a Linux system.Gained experience in identifying vulnerability and learned basic linux command while performing a simulated attack and defense scenerio.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux system</b> 
  

<h2>Environments Used </h2>

- <b>Attackbox</b>

<h2>Program walk-through:</h2>

<p align="center">
First we launch our vitual machine(vm) or attack box to start and load Linux: <br/>
<img src="https://i.imgur.com/pyLAfL2.png" height="80%" width="80%" alt="VM launch"/>
<br />
<br />
Now we are going to gatter some information about our target which is call Recon
we have his IP address which is 10.10.161.87 and for that we will used the nmap function:  <br/>
<img src="https://i.imgur.com/XtWryEG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next we are going to connect to the target server which will be ftp 10.10.161.87: <br/>
<img src="https://i.imgur.com/xePHV1Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We are going to try to login anonymous to see if FTP server support anonymous login:  <br/>
<img src="https://i.imgur.com/KxzAovR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
At this point we are going to see file avaible using the LS command:  <br/>
<img src="https://i.imgur.com/IVJf55u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now lets download the get of the file scret.txt to see what it contain using the GET command:  <br/>
<img src="https://i.imgur.com/HbLx51A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Since we have downloaded the file we are going to exit:  <br/>
<img src="https://i.imgur.com/ivb5CnE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next we are going to see the content of the secret.txt file by using the CAT command,and we found the password :  <br/>
<img src="https://i.imgur.com/d5jLAe7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
