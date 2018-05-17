ALL credit is given to Kinematics the original developer of the KParser program, and additionally to atom0s who identified the issue with why KParser would no longer read the game's memory or chat logs, in addition to being the original developer of the Memloc Finder program.


------------ These directions are also located in the "READ ME" file located in the Kparser Memloc Finder folder -----------

Directions:

For the program to be able to locate the new memloc, FFXI must be opened and it must also be running as pol.exe.


Most private servers use xiloader, or some other proprietary launcher, so you'll have to change the name and likely the location of it, your launch parameters in Ashita, or your settings.xml file for Windower to reflect these changes.


-----------------------------FOR ASHITA USERS-----------------------------
Create a folder within your Ashita Folder and name it something, I went with "nasomi-bootmod" to differentiate between the original folder path used which is "ffxi-bootmod" but you can name it whatever you want as long as it's reflected accurately in the line of text below.

now in the ffxi-bootmod folder, take the file boot.exe and place it into the folder you just created. Rename "boot" to "pol"

Open your Ashita settings for whichever profile you intend to use to launch the game with, add in the following line of text into the File field under Boot Configurations:

.\\nasomi-bootmod\\pol.exe


-----------------------------FOR WINDOWER USERS-----------------------------

Create a folder within your PlayOnline Folder and name it something, I went with "supernova-xiloader" you can name it whatever you want as long as it's reflected accurately in the line of text below.

now take the file xiloader.exe that should be in your PlayOnline folder and place it into the folder your just created. Rename "xiloader" to "pol"

Open your Windower settings.xml file in your choice of editing software(notepad++ works sufficiently) and add in this line of text between the <profile> </profile> tags for whichever profile you use to launch SuperNova or your private server:

<executable>.\\supernova-xiloader\\pol.exe</executable>


-----------------------------------------------------------------------------

Now the memloc finder "KparserMemloc.exe" should be able to locate the game whenever the file is ran. It should open a window similar to the command prompt. The letters and numbers following "Chat Memory Offset:" are what you're after. This is the memloc. The current version of the game is off by 8 bytes, so whatever numbers show up for the memloc, you will have to add 8 to it. They're displayed in hexadecimal though, and digits for hex only go up to 9 in numbers, then switch to letters following the number 9. So for example, say the memloc says it's 61bf33. Then the correct edit you make to the memloc in Kparser to reflect this would be 61bf3B. Because 3 + 8 = 11 

in Hexadecimal  A = 10
		B = 11
		C = 12   etc. all the way to the letter F

---------------------------------------------------------------------------------------------------------------

For the private server Nasomi 
the current chat memory offset the memloc finder gives you is: 61BF30

****the corrected memloc however(the one you input into Kparser)for this current version is: 61BF38
---------------------------------------------------------------------------------------------------------------

For the private server SuperNova 
the current chat memory offset the memloc finder gives you is: 61BF30

****the corrected memloc however(the one you input into Kparser)for this current version is: 61BF38
---------------------------------------------------------------------------------------------------------------

For All servers
In the KParser program itself take the memloc you acquired from the memloc finder input into the Tools > Options > Chat Log in RAM (Memory Offset address). Your KParser should now work.


***Every time the server gets updated with a new version, it will likely change the memloc. You will know this if Kparser no longer works. You will have to run the memloc finder again to find out the new memloc and add 8 to it like previously mentioned, to get KParser to be able to read the FFXI's memory again.
