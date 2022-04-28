## Powershell File Operations

Now that we know how to move in the file system, let's check how to manipulate files and folders. In this challenge, you will discover and use the commands **Get-Content, echo, New-Item, Move-Item, Copy-Item, and Remove-Item.**

* How to Create a file named story1.txt

`PS C:\Users\kasin> echo "Hello World" story1.txt`

* Type echo "Hello World" > story1.txt

* Print the content of the file

`PS C:\Users\kasin> echo "Hello World" story1.txt
Hello World`

* Create a folder named story

PS C:\Users\kasin>  New-Item -Path "c:\" -Name "story" -ItemType "directory"


    Directory: C:\


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        28-04-2022     13:42                story

* Move story1.txt inside story

PS C:\Users\kasin> Move-Item -Path C:\Users\kasin\story2.txt -Destination C:\Users\kasin\story1.txt

* Copy story1.txt as story2.txt

PS C:\Users\kasin> Copy-Item -Path "C:\Users\kasin\story1.txt" -Destination "C:\Users\kasin\story2.txt" -Recurse

* Print both files
<pre class="terminal">
PS C:\Users\kasin> Get-Content .\story1.txt
Hello World
PS C:\Users\kasin> Get-Content .\story2.txt
Hello World
</pre>

* Rename story2.txt as me.txt
PS C:\Users\kasin> Rename-Item -Path "c:\Users\kasin\story2.txt" -NewName "me.txt"
>> ls

## output

<pre class="terminal">
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
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
d-----        28-04-2022     13:42                story
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
-a----        28-04-2022     13:37             28 me.txt
-a----        28-04-2022     13:37             28 story1.txt
-a----        14-02-2022     13:13             39 Text-1.css
-a----        14-02-2022     16:46            271 Text-1.html
-a----        14-02-2022     13:38            405 Text-2.html
</pre>
* Append me.txt and add "I am a junior at Becode"

 PS C:\Users\kasin> cat me.txt
<pre class="terminal">
Hello World
I am a junior at Becode
<pre>

* Remove the folder story with it's content

PS C:\Users\kasin> Remove-Item story

Confirm
The item at C:\Users\kasin\story has children and the Recurse parameter was not specified. If you continue, all children will be removed with the item. Are you sure you want to continue?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

The folder will be removed from the terminal.
