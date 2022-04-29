## Powershell Package Management

It's time to start installing softwares and keep them updated. We will see how to use Chocolatey and how to use Windows Updates.

**Instructions**

* Get Windows updates

* Install the PSWindowsUpdate module

- Open Start.

- Search for PowerShell, right-click the top result, and select the Run as administrator option.

- Type the following command to download and install all the available updates and reboot the system, and press Enter:

`Get-WindowsUpdate -AcceptAll -Install -AutoReboot`

`Get-Package -Name PSWindowsUpdate`


* Type Get-WindowsUpdate to check for updates

`get-command -module PSWindowsUpdate`


* Manage Packages

To check the current Windows Update client settings, run the command:

`Get-WUSettings`

<pre class="terminal">
ComputerName                                 : WKS5S2N39S2
WUServer                                     : http://MN-WSUS:8530
WUStatusServer                               : http://MN-WSUS:8530
AcceptTrustedPublisherCerts                  : 1
ElevateNonAdmins                             : 1
DoNotConnectToWindowsUpdateInternetLocations : 1
TargetGroupEnabled                           : 1
TargetGroup                                  : ServersProd
NoAutoUpdate                                 : 0
AUOptions                                    : 3 - Notify before installation
ScheduledInstallDay                          : 0 - Every Day
ScheduledInstallTime                         : 3
UseWUServer                                  : 1
AutoInstallMinorUpdates                      : 0
AlwaysAutoRebootAtScheduledTime              : 0
DetectionFrequencyEnabled                    : 1
DetectionFrequency                         : 4
</pre>

* Install Chocolatey

In Windows Powershell Use the following command to install Chocolatey

<pre class="terminal">
Set-ExecutionPolicy Bypass -Scope Process -Force; `
  iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
</pre>

* Install VLC from Chocolatey

<pre class="terminal">
Restricting write permissions to Administrators
We are setting up the Chocolatey package repository.
The packages themselves go to 'C:\ProgramData\chocolatey\lib'
  (i.e. C:\ProgramData\chocolatey\lib\yourPackageName).
A shim file for the command line goes to 'C:\ProgramData\chocolatey\bin'
  and points to an executable in 'C:\ProgramData\chocolatey\lib\yourPackageName'.

Creating Chocolatey folders if they do not already exist.
</pre>

* Upgrade VLC to the latest version (it should already be but it's your first use)

1. Chocolatey

Chocolatey is a package manager for Windows. Package is just a fancy name for, what we call, software application or program. Examples of these include google chrome, firefox, vlc media player and skype. A package manager essentially makes the installation, updation and uninstallation of these programs very efficient by making the process error free and fast. In order to know more about chocolatey or package managers, you can visit chocolatey’s official website. Now we will look at how to install and use chocolatey.

2. Installing Chocolatey

The official guide to installing chocolatey has detailed instructions on how to install chocolatey. Over here I am going to summarize the process to save time, however, you can give the guide a read if you want. 

The first step is to open windows powershell as administrator. If you have not done that before; here is how to go about doing that: Click on the start button in windows and search for powershell by typing powershell; right click on the first result and select open as administrator. Inside powershell, copy and paste the following code and press enter:

Wait for the program to get installed and if you don’t see any errors within powershell, that means the installation was successful. In order to check if the program got installed correctly, close and reopen powershell as administrator and type the command choco and press enter:

`choco`

This should output the chocolatey version if the installation was successful. Please feel free to comment below if you run into trouble.

3. Installing software

Now comes the fun part. The first step is to search for the programs you want to install. You can do so at https://chocolatey.org/packages. In chocolatey there are a few options to install software. We can install one software application at a time or we can install multiple applications simultaneously:

<p class="terminal">
PS C:\Windows\system32> choco install vlc

Chocolatey v1.1.0
</pre>

* Remove the VLC package using Chocolatey

<pre class="terminal">
choco uninstall nodejs -y --remove-dependencies
Chocolatey v1.1.0
Uninstalling the following packages:
nodejs
</pre>

* Manage Windows Features

### Features

Deploy Anywhere You Have Windows/Cloud Ready (except Nano, sorry little buddy!). Yes, that includes Server.Core and Windows Docker Containers. Windows 7+/Windows 2003+ (although, we have been scaling down on 2003. I mean, 2003 is a bit long in the tooth, but some customers are still using it). Requires PowerShell v2+ (not PowerShell 6 yet - you're doing amazing if you are already on this, but give us some time) and Microsoft .NET Framework 4.x. You can deploy on prem, to Azure, AWS, or any cloud provider you might be looking at.

* Deploy with Everything. Anything that can manage endpoints or do remote deployments can either direct Chocolatey through commands, batches, or scripts. Full configuration management solutions like Ansible, Chef, PowerShell DSC, Puppet or Salt typically have providers/modules that allow you to work within their languages to manage both Chocolatey installation/configuration and software.

* All Software Is a First Class Citizen. You know how for most things, they only manage/report on the things installed in Add/Remove Programs (Programs and Features)? We count it all, because Windows software is more than just installers, and they all have security findings. So deploy your installers, your scripts, zips, runtime binaries, and yes, internal software all with one simple solution. Then lean on the reporting and inventory to be aware of all aspects of software you are managing.

* Packages are Independent and Portable. When you deploy through multiple systems or want to migrate from one to another, you can take the work you've done with Chocolatey with you. How is that for some major time-savings?

* Test Your Deployments. When's the last time you tested that deployment script you wrote for SCCM? Write it as a Chocolatey package instead and then you can test your infrastructure to be more comfortable when you push that change out to your constituents.

* Completely Offline and Secure. Chocolatey has zero call home, requires no network access to use (although we recommend for ease of management, you at least have internal network access!). Chocolatey does come with a default source that is the community repository. Turn that off and set up your own sources (FOR FREE). See our guide on organizational use to get started (it even has scripts!).

* Create Your Own Deployment Packages (FOR FREE) and, get this, use them internally (FOR FREE). Get started as simply as choco new <name> and then check out the "just in time" documentation interweaved right into the output!

* **PowerShell Automation**. You know those little scripts you've been writing for software deployments for years? Welcome to a breath of fresh air, you are going to love Chocolatey!

* Manage Dependencies With Ease. You ever have a very complex, specific installation order? It becomes suddenly very easy when you are using a package manager like Chocolatey. Then you can concentrate on harder problems, like what flavor to add to your coffee today.

* Open Source Licensing Is Ready for Business. We have Apache v2 licensing, no special restrictions need apply. Our commercial options come with a more business friendly Software License agreement (and yes, we do have a redline format).

* Commercial Options Add Support + AMAZING Features. Our top of the line Chocolatey for Business (C4B) edition includes over 20+ features that take Chocolatey to the next level and make it a full software management solution and not just a package manager. Go ahead, right click on an installer and create a fully unattended software deployment in 5 seconds! If you have any issues, our support team is ready and waiting to help you move forward.

* Customers Help Define Our Work. We determine and prioritize our work based on where customers want things to go. We are building a platform, and we are working with you to make it better.

* Security Is Our Focus. Take a stroll through our security page. With everything we design, we focus on simplicity, scalability, and security.

* Bridge the Gap. Have you started to look at moving from those legacy automation systems to something more modern like Ansible, Puppet, or Chef and didn't know where to start? Start shifting the software management over to Chocolatey and taking those existing infrastructure/end point management tools back to just the remote deployment. Then when you are ready, you shift over to those modern automation solutions without needing to rewrite everything! Those Chocolatey packages work with all systems!

* Scale With Ease. There are massive deployments of Chocolatey, even the open source edition, in large enterprises. Chocolatey is deployed in everything from small startups all the way up to those fortune 500 companies.


* Get installed windows features with the command Get-WindowsFeature

<pre class="terminal">
Get-WindowsFeature
   [[-Name] <String[]>]
   [-Vhd <String>]
   [-ComputerName <String>]
   [-Credential <PSCredential>]
   [-LogPath <String>]
   [<CommonParameters>]

</pre>

**Description**

The *Get-WindowsFeature* cmdlet gets information about features that are both available for installation and already installed on a computer that is running Windows Server or an offline virtual hard disk (VHD) that is running Windows Server.

Examples

<pre class="terminal">
PowerShell

Copy
`Get-WindowsFeature -ComputerName Server1 -Credential contoso.com\user1`
</pre>

This example gets a list of features that is available and installed on the target computer named Server1. The credentials for user user1 in the Contoso.com domain, a user who has Administrator rights on Server1, are provided.

* Install a new feature such as hyper-v with Install-WindowsFeature

1. On the Windows desktop, click the Start button and type any part of the name Windows PowerShell.

2. Right-click Windows PowerShell and select Run as Administrator.

3. To install Hyper-V on a server you're connected to remotely, run the following command and replace <computer_name> with the name of server.

<pre class="terminal">
PowerShell

Copy

Install-WindowsFeature -Name Hyper-V -ComputerName <computer_name> -IncludeManagementTools -Restart
If you're connected locally to the server, run the command without -ComputerName <computer_name>.

</pre>

4. After the server restarts, you can see that the Hyper-V role is installed and see what other roles and features are installed by running the following command:

<pre class="terminal">
PowerShell

Copy

Get-WindowsFeature -ComputerName <computer_name>

</pre>

5. If you're connected locally to the server, run the command without -ComputerName <computer_name>.



