# Installing and Using OpenGD77CPS

## Richie Jarvis - G1ZNE - 2025-02-20

<span style="color:red">
      
NOTE ON PROGRAMMING CABLES!

DM-1701 works with DM-1801 and RD-5R cables, basically other Baofeng direct USB cables.
It does not work with Baofeng UV-5R etc cables that have a USB to Serial converter chip in the plug.

Used the following Video to figure this out if you prefer video learning: https://www.youtube.com/watch?v=gW-OH-j2it4

</span>

1. 	Get a DMR ID here: https://radioid.net/
1. 	If in Chinese Language
	- Green button to get into Menu
	- Utilities (Spanner Icon) then Green
	- Item 1 then Green
	- Item 8 then Green
	- There are 2 options - Top option then Green, which selects English
1. 	Download the latest copy of CPS from: https://www.opengd77.com/viewforum.php?f=12 - the "Announcements" section shows the latest version.
1. 	Download from drive.proton.me (the site currently in use for the software.  It may change in future)
	- Note: Google Chrome downloaded the file, BUT it didn't rename it from "Unconfirmed blah blah blah.crdownload".  I manually renamed the crdownload file to "OpenGD77CPSInstaller.exe" and then it worked.
1. 	I did a completely standard install.  I left "Install penGD77 Comm port driver" ticked.
1. 	OpenGD77CPS started automagically eventually
1. 	Accept the warning
1. 	Login to the website: https://radioid.net/login to create/retrieve your DMR ID.  I signed up for mine a while back.  I think I had to send in a copy of my HAM licence PDF from Ofcom.
1. 	You will find 2 driver files on the website https://www.opengd77.com/downloads/drivers/  Download and install them both.
1. 	Start OpenGD77CPS
1. 	Change the Radio type to "MD9600,RT-90/MD-UV380/RT3S,DM-1701/RT-84,MD-2017/RT-82" - the second option.  More radios might be listed in the future.
1. 	Follow the instructions here: https://www.opengd77.com/viewtopic.php?f=19&t=2380
1. 	Where it says to "Backup Flash" and it is very important, do not skip this step!  Your radio should be in normal mode, not in the Firmware Loader mode.  The Green light should be on.  
1. 	Open the "Program" menu item, click "Cancel" if it asks for a COM port, and the OpenGD77 Support page will open.  Click "Backup Flash".  The process will start, and the Radio will display "CPS Backup Flash" on the radio screen.  The CPS will display "Reading Flash" and the green progress bar will show the progress.  Wait for it to complete.
1. 	The "Save" dialog will appear.  Name the file something you can find later if you need to.  Save it somewhere safe.
1. 	Continue with the instructions on the https://www.opengd77.com/viewtopic.php?f=19&t=2380 page
1. 	Backup the default codeplug.  In the OpenGD77 Support window, click "Read codeplug".  Mine displayed:
 
	```
	Your codeplug uses 16 channel zones.  It will be automatically updated to 80 channel zones.  
	Please check the Zones to ensure the update worked correctly before saving or uploading the codeplug"
	Click "OK"
	```
			
	Click `File` then `Save`.  Find a place to save it.		
		
1. Download my blank codeplug from here: https://github.com/richiejarvis/ham/blob/main/Digital_Modes/DMR/Blank_2025-02-22_2244_Codeplug_Iteration_8.g77 and save it.  Load it into the OpenGD77CPS using the `File` then `Open` menu.

This codeplug contains the following setup - `code style` names are the names in the CPS.

	- `DMR ID and Callsign` set to `YOURS` & `1`
	- All Analogue Simplex 2m `Channels` from this list: https://hamradiosouthernrepeaters.co.uk/images/PDF/Simplex_Channel_Frequency.pdf
	- Analogue Simplex  70cms `Channels` from this list: https://hamradiosouthernrepeaters.co.uk/images/PDF/Simplex_Channel_Frequency.pdf
	- All Analogue Repeater 2m & 70cms `Channels` with a CTCSS code of 88.5 - Change to taste for your local repeaters.
	- The following South East area repeaters with the correct CTCSS code pre-set:
		- GB3LR
		- GB3HY
		- GB3HE
		- GB7ZE
		- GB3MH
		- GB3ES
		- GB3WS
		- GB7RX
	- DMR GB7ZE `TG List
	- WPSD HotSpot `TG Group List`
		- Both TalkGroup List's contain the following `Digital Contacts`
			- Groups - Time Slot (TS) 1
				- Local TG 9 (Call ID 9)
			- Groups - Time Slot (TS) 2
				- South East (Call ID 23510)
				- Kent Chat (Call ID 23519)
				- UK Chat Main (Call ID 2350)
				- UK Chat 1 (Call ID 2351)
				- UK Chat 2 (Call ID 2352)
				- UK Chat 3 (Call ID 2353)
				- Ireland Chat (Call ID 2354)
				- Scotland Chat (Call ID 2355)
				- Wales Chat (Call ID 2356)
				- HUBNet (Call ID 23526)
				- World-Wide (Call ID 91)
				- World-Wide TAC 1 (Call ID 901)
				- World-Wide TAC 2 (Call ID 902)
				- World-Wide TAC 3 (Call ID 903)
			- Private Call - Time Slot (TS 1)
				- PARROT (Call ID 9990) - Use this to test - Press PTT, Talk, and it will "Parrot" your audio back to you.
			- Private Call - Time Slot (TS 2)
				- DISCONNECT (Call ID 4000) - __I've not figured out what this one does yet?__

1. Double click on "DMR ID and callsign" on the left hand side of the CPS, and enter your Callsign and DMR ID.

1. Connect your Baofeng DM-1701 (or other OpenGD77 supported radio) and select menu item `Program` then `Write`.

1. Try the radio with GB7ZE or Hotspot.
