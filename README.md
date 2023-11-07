<h1>Install Suricata</h1>


<h2>Description</h2>
In this project we will install Suricata IDS to monitor an existing Nextcloud server instance and test to make sure it is working correctly. This installation will be done on a Linux cloud VM currently running the Nextcloud instance. 
<br />


<h2>Environments Used: </h2>

- <b>Ubuntu 20.04 LTS</b>

<h2>Installation walk-through:</h2>

<p align="center">
After logging in to the server we will need to add the repository for Suricata: <br/>
<img src="https://i.imgur.com/9QS6kl7.png" height="80%" width="80%" alt="Add Repo"/>
<br />
<br />
We will need to run apt-update and then install suricata:  <br/>
<img src="https://i.imgur.com/FN4hiJQ.png" height="80%" width="80%" alt="Update and Install"/>
<br />
<br />
Once the install is complete we will enable Suricata using systemctl then stop the service temporarily so we can configure it: <br/>
<img src="https://i.imgur.com/uynGLFe.png" height="80%" width="80%" alt="Enable Suricata"/>
<br />
<br />
Next we will check the default interface we want to monitor on to update the config file. Note the interface is eth0:  <br/>
<img src="https://i.imgur.com/FfyYKfA.png" height="80%" width="80%" alt="Check Default Interface"/>
<br />
<br />
We will then open the configuration file with nano to edit the configuration:  <br/>
<img src="https://i.imgur.com/0gW5qQ5.png" height="80%" width="80%" alt="Open Config File"/>
<br />
<br />
Next we will edit the interface to match our system, in this case it is eth0:  <br/>
<img src="https://i.imgur.com/Dh86zWI.png" height="80%" width="80%" alt="Edit interface in config file"/>
<br />
<br />
The rule set will then need to be updated so we have updated rules for Suricata to use to monitor the network:  <br/>
<img src="https://i.imgur.com/YMIuuYE.png" height="80%" width="80%" alt="Update Suricata Rules"/>
<br />
<br />
Since updating the config and rules we will test the configuration and once successfull will then start the Suricata service:  <br/>
<img src="https://i.imgur.com/XDrkJK6.png" height="80%" width="80%" alt="Test and start Suricata"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
