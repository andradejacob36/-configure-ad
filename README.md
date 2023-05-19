<p align="center">
<img src="https://i.imgur.com/XQf7h39.png" height="50%" width="50%"/>
</p>

<h1>Setting up & Using Proton VPN on Azure: A Comprehensive Guide</h1>
This tutorial outlines the implementation of Proton VPN within an Azure Virtual Machine.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Proton VPN
- WhatIsMyIPAddress.com

<h2>Operating Systems Used </h2>

- Windows 10 Pro, version 21H2 (free services eligible)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Confirm your IPv4 address and city location on your computer
- Step 2: Set up an Azure Virtual Machine and ensure it meets the system requirements for Proton VPN
- Step 3: Re-verify your computer's IPv4 address and city location
- Step 4: Download and install Proton VPN on the Azure Virtual Machine
- Step 5: Ensure that Proton VPN is working correctly by performing a connectivity test and verifying that your IP address has been changed

<h2>Step 1: Confirm your IPv4 address and city location on your computer</h2>

1.Before we create an Azure VM, we will need to verify our own IP Address with the following link: https://whatismyipaddress.com/

- Note: Copy down the provided details of your IPv4 and city to a notepad. 

<p>
<img src="https://i.imgur.com/PNMOtSk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
<h2>Step 2: Set up an Azure Virtual Machine and ensure it meets the system requirements for Proton VPN</h2>

1.Go to the Azure Portal website (https://portal.azure.com/) and sign-in with your Azure account credentials. 

- Note: If you do not have an Azure account, you will need to sign-up for one before you can log-in.

2.Click on the search bar and type "Virtual Machines".

3.Click on the "+ Create" button located on the top left-corner by "Switch to classic".

4.Choose the option "Azure virtual machine", enter the following information:
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
<img src="https://i.imgur.com/ggc9djW.png" height="80%" width="80%"/>
</p>
<p>  

5.On the search bar, type "Virtual Machines".

- Note: After you created your VM, you should be able to see the following display:

<p>
<img src="https://i.imgur.com/bOxI92i.png" height="80%" width="80%"/>
</p>
<p>  

6.Click the blue link "vm-practice" located under "Name".

7.On the "Overview" tab, find/copy the Public IP address located under "Size"; Essentials.

<p>
<img src="https://i.imgur.com/42QEZ5z.png" height="80%" width="80%"/>
</p>
<p>  

8.To access Remote Desktop Connection on Windows, navigate to the bottom-left corner and click on the "Start" button (Windows logo), then search for "Remote Desktop Connection" and open it. For Mac users download the app "remote- Microsoft Remote Desktop" from the App Store.

9.Paste the Public IP address(from your VM) in the computer name field and click "Connect". For Mac users paste the IP Address on "PC-name" and click "add".

<p>
<img src="https://i.imgur.com/5UYpYcR.png" height="80%" width="80%"/>
</p>
<p>  

10.Afterwards, make sure to log-in your credentials from Step 3 (Use Username: labuser/Password: Your unique password).

- Note: For Windows users click "Yes" to connect to your VM. Observe the following display: 

<p>
<img src="https://i.imgur.com/xHG3t9h.png" height="80%" width="80%"/>
</p>
<p>  

11.Please wait until your virtual machine logs you in.

12.Then choose the following options for "Choose privacy settings for your device": 
    <ol type="a">
      <li>Location: No </li>
      <li>Diagnostic Data: No</li>
      <li>Tailored experiences: No</li>
      <li>Find my device: No</li>
     <li>Inking and Typing: No</li>
     <li>Advertising ID: No</li>
    </ol>

13.Click "Accept"   

<h2>Step 3: Re-verify your computer's IPv4 address and city location</h2>

1.On your VM, browse Microsoft Edge and paste the following link: https://whatismyipaddress.com/

- Note: Copy down the provided details of your VM's IPv4 and city to a notepad. 

<p>
<img src="https://i.imgur.com/PM8yEpv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h2>Step 4: Download and install Proton VPN on the Azure Virtual Machine</h2>

1.On your VM, open Microsoft Edge and paste the following link: https://account.protonvpn.com/signup?plan=free&language=en

2.Create a free account. Aftewards, click the "Download" button under Windows.

<p>
<img src="https://i.imgur.com/gzjFT5Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

3.Proceed by clicking "Download Proton VPN".

<p>
<img src="https://i.imgur.com/5bt61rr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

4.After downloading Proton VPN, go to Downloads; File Explorer.

5.Double-click "ProtonVPN_win_v2.4.1"

<p>
<img src="https://i.imgur.com/NJEihw0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

6.Navigate through the settings and finish installing the application. 

<h2>Step 5: Ensure that Proton VPN is working correctly by performing a connectivity test and verifying that your IP address has been changed</h2>

1.Click on the Windows logo and type "Proton VPN" to find the application.

2.After launching the application, use your email and unique password to log-in.

- Note: We're going to test it by connecting our server (France Central) to a random Japanese Server.

3.Next to Japan, click "Connect" to connect to a Japanese server.

<p>
<img src="https://i.imgur.com/bMNBH5y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>   

<p>
<img src="https://i.imgur.com/n6u78j0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>   

4.With the following link confirm your new IP address connected to the Japanese Server: https://whatismyipaddress.com/

<p>
<img src="https://i.imgur.com/cmJy5vD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>   

5.Congratulations, you have created a VPN tunnel from your local server (France Central) to the VPN server in Japan. 
