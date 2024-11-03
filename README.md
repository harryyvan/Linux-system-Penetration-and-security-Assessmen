
<h1>Linux system Penetration and security Assessment(Tryhackme)</h1>
<h1>JWipe - Disk Sanitization</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
My project consiste of engaging in a control environmennt using Tryhackme attackbox to understand the process of accessing and securing a Linux system.Gained experience in identifying vulnerability and learned basic linux command while performing a simulated attack and defense scenerio.
Project consists of a simple PowerShell script that walks the user through "zeroing out" (wiping) any drives that are connected to the system. The utility allows you to select the target disk and choose the number of passes that are performed. The PowerShell script will configure a diskpart script file based on the user's selections and then launch Diskpart to perform the disk sanitization.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux system</b> 
  
- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Environments Used </h2>

- <b>Attackbox</b>
- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
First we launch our vitual machine(vm) or attack box to start and load Linux: <br/>
<img src="https://i.imgur.com/pyLAfL2.png" height="80%" width="80%" alt="VM launch"/>
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now we are going to gatter some information about our target which is call Recon
we have his IP address which is 10.10.161.87 and for that we will used the nmap function:  <br/>
<img src="https://i.imgur.com/XtWryEG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next we are going to connect to the target server which will be ftp 10.10.161.87: <br/>
<img src="https://i.imgur.com/xePHV1Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
We are going to try to login anonymous to see if FTP server support anonymous login:  <br/>
<img src="https://i.imgur.com/KxzAovR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
At this point we are going to see file avaible using the LS command:  <br/>
<img src="https://i.imgur.com/IVJf55u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now lets download the get of the file scret.txt to see what it contain using the GET command:  <br/>
<img src="https://i.imgur.com/HbLx51A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Since we have downloaded the file we are going to exit:  <br/>
<img src="https://i.imgur.com/ivb5CnE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next we are going to see the content of the secret.txt file by using the CAT command,and we found the password :  <br/>
<img src="https://i.imgur.com/d5jLAe7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
@@ -58,4 +55,3 @@ Next we are going to see the content of the secret.txt file by using the CAT com
# text in gray
@@ text in purple (and bold)@@
```
