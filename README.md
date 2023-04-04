<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Setting up & Using Proton VPN on Azure: A Comprehensive Guide</h1>
This tutorial outlines the implementation of Proton VPN within an Azure Virtual Machine.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Proton VPN

<h2>Operating Systems Used </h2>

- Windows 10 Pro, version 21H2 (free services eligible)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Set up an Azure Virtual Machine and ensure it meets the system requirements for Proton VPN
- Step 2: Download and install Proton VPN on the Azure Virtual Machine
- Step 3: Set up the necessary configurations such as selecting the VPN server, establishing connection protocol, and configuring DNS settings
- Step 4: Ensure that Proton VPN is working correctly by performing a connectivity test and verifying that your IP address has been changed
- Step 5: Configure the VPN to automatically connect when the Virtual Machine starts up.

<h2>Step 1: Set up an Azure Virtual Machine and ensure it meets the system requirements for Proton VPN</h2>

1. Before we create an Azure VM, we will need to verify our own IP Address with the following link: https://whatismyipaddress.com/

- Note: Copy down the provided details of your IPv4 and city to a notepad. 

- Image display of Step 1: 1
<p>
<img src="https://i.imgur.com/PNMOtSk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

2. Go to the Azure Portal website (https://portal.azure.com/) and sign-in with your Azure account credentials. 
- Note: If you do not have an Azure account, you will need to sign-up for one before you can log-in.

3. Click on the search bar and type "Virtual Machines".
4. Click on the "+ Create" button located on the top left-corner by "Switch to classic".
5. Choose the option "Azure virtual machine", enter the following information:
    <ol type="a">
      <li>Choose your subscription (For Ex: Azure Subscription 1).</li>
      <li>Enter a unique name for the virtual machine (Use: vm-practice).</li>
      <li>For "Region" select:(Europe) France Central (Note: Don't select the region you live in).</li>
      <li>For "Resource group" it should automatically create a unique name.</li> 
      <li>For "Image" use: Windows 10 Pro, version 21H2 (free services eligible). </li>
      <li>For "Size" use: Standard_E2s_v3 - 2 vcpus, 16 GiB memory. </li>
      <li>For "Username" use: labuser.</li>
      <li>For "Password" make sure to make up one.</li>
      <li>For "Public inbound ports" click on "Allow selected ports".</li>
      <li>For "Select inbound ports" use: RDP 3389.</li>
    </ol>

- Note: After you checkmarked "I confirm I have an eligible Windows 10/11 license with multi-tenant hosting rights. Please confirm." located at bottom-left corner. Also, after you clicked on the "Review + create" button and review the settings. You should be able to see the following display:
<p>
<img src="" height="80%" width="80%"/>
</p>
<p>  
    
6. On the search bar, type "Virtual Machines".
- Note: After you created your VM, you should be able to see the following display:

<p>
<img src="" height="80%" width="80%"/>
</p>
<p>  

7. Click the blue link "" located under "Name".
8. On the "Overview" tab, find/copy the Public IP address located under "Size"; Essentials.
<p>
<img src="" height="80%" width="80%"/>
</p>
<p>  

9. To access Remote Desktop Connection on Windows, navigate to the bottom-left corner and click on the "Start" button (Windows logo), then search for "Remote Desktop Connection" and open it. For Mac users download the app "remote- Microsoft Remote Desktop" from the App Store.
 
10. Paste the Public IP address(from your VM) in the computer name field and click "Connect". For Mac users paste the IP Address on "PC-name" and click "add".
 
<p>
<img src="" height="80%" width="80%"/>
</p>
<p>  
 
11. Afterwards, make sure to log-in your credentials from Step 3 (Use Username: labuser/Password: Your unique password).

- Note: For Windows users click "Yes" to connect to your VM. Observe the following display: 
<p>
<img src="https://i.imgur.com/xHG3t9h.png" height="80%" width="80%"/>
</p>
<p>  
 
12. Please wait until your virtual machine logs you in.
13. Then choose the following options for "Choose privacy settings for your device": 
    <ol type="a">
      <li>Location: No </li>
      <li>Diagnostic Data: No</li>
      <li>Tailored experiences: No</li>
      <li>Find my device: No</li>
     <li>Inking and Typing: No</li>
     <li>Advertising ID: No</li>
    </ol>

14. Click "Accept"   
  
