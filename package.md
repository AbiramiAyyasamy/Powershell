## Powershell Package Management

* It's time to start installing softwares and keep them updated. We will see how to use Chocolatey and how to use Windows Updates.

**Instructions**

* Get Windows updates

* Install the PSWindowsUpdate module

- Open Start.

- Search for PowerShell, right-click the top result, and select the Run as administrator option.

- Type the following command to download and install all the available updates and reboot the system, and press Enter: Get-WindowsUpdate -AcceptAll -Install -AutoReboot.

`Get-Package -Name PSWindowsUpdate`


* Type Get-WindowsUpdate to check for updates
`get-command -module PSWindowsUpdate`



* Type Install-WindowsUpdate to install updates

Install-WindowsUpdate -MicrosoftUpdate -AcceptAll -AutoReboot




* Manage Packages

To check the current Windows Update client settings, run the command:

Get-WUSettings
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
<pre>

* Install Chocolatey

* Install VLC from Chocolatey

* Upgrade VLC to the latest version (it should already be but it's your first use)

* Remove the VLC package using Chocolatey

* Could you use Chocolatey on already installed software? How?

* Manage Windows Features

* Get installed windows features with the command Get-WindowsFeature

* Install a new feature such as hyper-v with Install-WindowsFeature
