## Powershell Navigation
Now we will learn how to move around in the filesystem with **Set-Location, Get-Location, Get-ChildItem ...**

* Print your current location on the screen
<pre class ="terminal">
PS C:\Users\kasin> Get-Location

Path
----
C:\Users\kasin

</pre>

* Print the content of your current directory
`Get-ChildItem`

<p class ="terminal">

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        13-04-2022     11:21                .ssh
d-----        28-03-2022     11:30                .vscode
d-r---        26-12-2021     14:42                3D Objects
d-----        22-04-2022     11:52                bashscripts
d-----        14-04-2022     16:35                cadavrexquis
d-r---        26-12-2021     14:42                Contacts
d-----        27-04-2022     09:32                Documents
d-r---        27-04-2022     14:15                Downloads
d-r---        26-12-2021     14:42                Favorites
da----        28-03-2022     11:37                javascript
d-r---        26-12-2021     14:42                Links
d-r---        26-12-2021     14:42                Music
d-----        13-04-2022     11:59                new.org
dar--l        28-04-2022     09:04                OneDrive
d-----        25-04-2022     20:10                Pictures
d-r---        26-12-2021     14:42                Saved Games
d-----        28-03-2022     10:22                scrap
d-r---        26-12-2021     14:43                Searches
d-r---        27-01-2022     12:59                Videos
-a----        25-04-2022     16:37           8216 .bash_history
-a----        22-04-2022     11:50            341 .gitconfig
-a----        14-04-2022     19:43             20 .lesshst
-a----        07-03-2022     13:25             74 .node_repl_history
-a----        23-02-2022     17:48            103 48.css
-a----        23-02-2022     17:56            321 50.html
-a----        23-02-2022     16:15            432 51.html
-a----        25-02-2022     11:52            200 52.html
-a----        14-02-2022     14:23            389 BOLD.html
-a----        14-04-2022     16:31           2501 code.txt
-a----        14-02-2022     15:24            182 depart.html
-a----        14-02-2022     14:00            510 exemple.html
-a----        14-02-2022     13:54            404 intro.html
-a----        14-02-2022     14:15            455 LINEBREAK.html
-a----        14-02-2022     15:13            653 list.html
-a----        08-04-2022     09:27          12533 login.html
-a----        28-04-2022     14:00             78 me.txt
-a----        28-04-2022     13:37             28 story1.txt
-a----        14-02-2022     13:13             39 Text-1.css
-a----        14-02-2022     16:46            271 Text-1.html
-a----        14-02-2022     13:38            405 Text-2.html

</pre>

* Print the content of your root (C: if you're running windows, / for linux)

   Directory: C:\Users

<pre class="terminal">

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        12-02-2022     22:47                defaultuser100000
d-----        12-02-2022     22:47                defaultuser100000.DESKTOP-VJ89FK4
d-----        12-02-2022     22:47                defaultuser100000.DESKTOP-VJ89FK4.000
d-----        12-02-2022     22:47                defaultuser100001
d-----        12-02-2022     22:47                defaultuser100001.DESKTOP-VJ89FK4
d-----        12-02-2022     22:47                defaultuser100001.DESKTOP-VJ89FK4.000
d-----        12-02-2022     22:47                defaultuser100001.DESKTOP-VJ89FK4.001
d-----        12-02-2022     22:47                defaultuser100001.DESKTOP-VJ89FK4.002
d-----        28-04-2022     14:17                kasin
d-r---        24-08-2021     12:57                Public
</pre>
* Go into your home folder (C:\Users\Username or /home/Username)

* Print the content of your home

* Those commands are pretty long to type, do you know any shorter way to do it?

`alias`
<pre class="terminal">

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           % -> ForEach-Object
Alias           ? -> Where-Object
Alias           ac -> Add-Content
Alias           asnp -> Add-PSSnapin
Alias           cat -> Get-Content
Alias           cd -> Set-Location
Alias           CFS -> ConvertFrom-String                          3.1.0.0    Microsoft.PowerShell.Utility
Alias           chdir -> Set-Location
Alias           clc -> Clear-Content
Alias           clear -> Clear-Host
Alias           clhy -> Clear-History
Alias           cli -> Clear-Item
Alias           clp -> Clear-ItemProperty
Alias           cls -> Clear-Host
Alias           clv -> Clear-Variable
Alias           cnsn -> Connect-PSSession
Alias           compare -> Compare-Object
Alias           copy -> Copy-Item
Alias           cp -> Copy-Item
Alias           cpi -> Copy-Item
Alias           cpp -> Copy-ItemProperty
Alias           curl -> Invoke-WebRequest
Alias           cvpa -> Convert-Path
Alias           dbp -> Disable-PSBreakpoint
Alias           del -> Remove-Item
Alias           diff -> Compare-Object
Alias           dir -> Get-ChildItem
Alias           dnsn -> Disconnect-PSSession
Alias           ebp -> Enable-PSBreakpoint
Alias           echo -> Write-Output
Alias           epal -> Export-Alias
Alias           epcsv -> Export-Csv
Alias           epsn -> Export-PSSession
Alias           erase -> Remove-Item
Alias           etsn -> Enter-PSSession
Alias           exsn -> Exit-PSSession
Alias           fc -> Format-Custom
Alias           fhx -> Format-Hex                                  3.1.0.0    Microsoft.PowerShell.Utility
Alias           fl -> Format-List
Alias           foreach -> ForEach-Object
Alias           ft -> Format-Table
Alias           fw -> Format-Wide
Alias           gal -> Get-Alias
Alias           gbp -> Get-PSBreakpoint
Alias           gc -> Get-Content
Alias           gcb -> Get-Clipboard                               3.1.0.0    Microsoft.PowerShell.Management
Alias           gci -> Get-ChildItem
Alias           gcm -> Get-Command
Alias           gcs -> Get-PSCallStack
Alias           gdr -> Get-PSDrive
Alias           ghy -> Get-History
Alias           gi -> Get-Item
Alias           gin -> Get-ComputerInfo                            3.1.0.0    Microsoft.PowerShell.Management
Alias           gjb -> Get-Job
Alias           gl -> Get-Location
Alias           gm -> Get-Member
Alias           gmo -> Get-Module
Alias           gp -> Get-ItemProperty
Alias           gps -> Get-Process
Alias           gpv -> Get-ItemPropertyValue
Alias           group -> Group-Object
Alias           gsn -> Get-PSSession
Alias           gsnp -> Get-PSSnapin
Alias           gsv -> Get-Service
Alias           gtz -> Get-TimeZone                                3.1.0.0    Microsoft.PowerShell.Management
Alias           gu -> Get-Unique
Alias           gv -> Get-Variable
Alias           gwmi -> Get-WmiObject
Alias           h -> Get-History
Alias           history -> Get-History
Alias           icm -> Invoke-Command
Alias           iex -> Invoke-Expression
Alias           ihy -> Invoke-History
Alias           ii -> Invoke-Item
Alias           ipal -> Import-Alias
Alias           ipcsv -> Import-Csv
Alias           ipmo -> Import-Module
Alias           ipsn -> Import-PSSession
Alias           irm -> Invoke-RestMethod
Alias           ise -> powershell_ise.exe
Alias           iwmi -> Invoke-WmiMethod
Alias           iwr -> Invoke-WebRequest
Alias           kill -> Stop-Process
Alias           lp -> Out-Printer
Alias           ls -> Get-ChildItem
Alias           man -> help
Alias           md -> mkdir
Alias           measure -> Measure-Object
Alias           mi -> Move-Item
Alias           mount -> New-PSDrive
Alias           move -> Move-Item
Alias           mp -> Move-ItemProperty
Alias           mv -> Move-Item
Alias           nal -> New-Alias
Alias           ndr -> New-PSDrive
Alias           ni -> New-Item
Alias           nmo -> New-Module
Alias           npssc -> New-PSSessionConfigurationFile
Alias           nsn -> New-PSSession
Alias           nv -> New-Variable
Alias           ogv -> Out-GridView
Alias           oh -> Out-Host
Alias           popd -> Pop-Location
Alias           ps -> Get-Process
Alias           pushd -> Push-Location
Alias           pwd -> Get-Location
Alias           r -> Invoke-History
Alias           rbp -> Remove-PSBreakpoint
Alias           rcjb -> Receive-Job
Alias           rcsn -> Receive-PSSession
Alias           rd -> Remove-Item
Alias           rdr -> Remove-PSDrive
Alias           ren -> Rename-Item
Alias           ri -> Remove-Item
Alias           rjb -> Remove-Job
Alias           rm -> Remove-Item
Alias           rmdir -> Remove-Item
Alias           rmo -> Remove-Module
Alias           rni -> Rename-Item
Alias           rnp -> Rename-ItemProperty
Alias           rp -> Remove-ItemProperty
Alias           rsn -> Remove-PSSession
Alias           rsnp -> Remove-PSSnapin
Alias           rujb -> Resume-Job
Alias           rv -> Remove-Variable
Alias           rvpa -> Resolve-Path
Alias           rwmi -> Remove-WmiObject
Alias           sajb -> Start-Job
Alias           sal -> Set-Alias
Alias           saps -> Start-Process
Alias           sasv -> Start-Service
Alias           sbp -> Set-PSBreakpoint
Alias           sc -> Set-Content
Alias           scb -> Set-Clipboard                               3.1.0.0    Microsoft.PowerShell.Management
Alias           select -> Select-Object
Alias           set -> Set-Variable
Alias           shcm -> Show-Command
Alias           si -> Set-Item
Alias           sl -> Set-Location
Alias           sleep -> Start-Sleep
Alias           sls -> Select-String
Alias           sort -> Sort-Object
Alias           sp -> Set-ItemProperty
Alias           spjb -> Stop-Job
Alias           spps -> Stop-Process
Alias           spsv -> Stop-Service
Alias           start -> Start-Process
Alias           stz -> Set-TimeZone                                3.1.0.0    Microsoft.PowerShell.Management
Alias           sujb -> Suspend-Job
Alias           sv -> Set-Variable
Alias           swmi -> Set-WmiInstance
Alias           tee -> Tee-Object
Alias           trcm -> Trace-Command
Alias           type -> Get-Content
Alias           wget -> Invoke-WebRequest
Alias           where -> Where-Object
Alias           wjb -> Wait-Job
Alias           write -> Write-Output
</pre>
