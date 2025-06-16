<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Installation Configuration</h1>
This tutorial outlines the recommended post-installation configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Post-Installation</h2>

<p>
</p>
<p>
Now that we have successfully installed osTicket alongside all it's dependencies we can focus on systems administration. There are two links that will be important for this section. The first: http://localhost/osTicket/scp/login.php is the admin login page from where you can login using the admin account created on the first part of this tutorial, we will do most all of the configurations from this side of osTicket. The second: http://localhost/osTicket is the end-user side of osTicket from where tickets can be submitted for you to work on. 

 *(If you are working on a Windows laptop already you can skip the first three steps and starts at step four (IIS))*
</p>
<p>
In Azure, create a resource group and title it "osTicketrg" then a virtual network under that same resource group titled "osticketrg-vnet". Afterwards create a VM with 2 vcpus, 8 GiB Memory and put it under the same resource group.
</p>
<p align="center">
 <img alt="Screenshot 2025-05-29 at 11 36 38 AM" src="https://github.com/user-attachments/assets/b5acbb0b-579f-4f38-b558-d1ced7d62c7c" height="80%" width="80%" />
</p>
<br />
<p>
</p>
