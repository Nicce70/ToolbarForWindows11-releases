# Toolbar For Windows 11---release
Creates a Toolbar at the top of the screen on Windows 11. Use with ex. Windhawk's Modd 'Taskbar on top for Windows 11' 

----------------------------------
INSTALL:
----------------------------------
This is a stand alone program.

1. Download and unzip the .zip file.

2. Copy the entire ToolbarForWindows11 folder to e.g.
C:\Program Files\ - (You will need admin rights and you have to run the program as admin)
or put it in e.g. "My Documents\" then it should work without admin rights.

3. Run "ToolbarForWindows11.exe"

----------------------------------
User Guide
----------------------------------
Right-click on ToolbarForWindows11 to bring up the menu, which includes Settings, Exit and also the Restart Explorer.exe function (if you have problems with the Windows 11 taskbar losing characters or other things).
Under Settings there are instructions on how to add programs to Toolbar etc.

----------------------------------
USE IN COMBINATION WITH WINDHAWK:
----------------------------------
If you use ToolbarForWindows11 in combination with WindHawk and with the Modd "Taskbar on top for Windows 11", you need to make the Windows 11 taskbar move down a bit from the top of the screen so that the Toolbar can fit without overlapping each other. You do this by modifying the Modd "Taskbar on top for Windows 11" in the following places, in this case it is moved down 50 pixels (you can adjust this according to your own settings and taste):

Line 505: windowpos->y = monitorRect.top;

to: windowpos->y = monitorRect.top + 50; 

Line 679: rectNew.Y = monitorInfo.rcWork.top + MulDiv(12, monitorDpiY, 96);

to: rectNew.Y = monitorInfo.rcWork.top + 50 + MulDiv(12, monitorDpiY, 96);

Line 1239: Y = monitorInfo.rcWork.top + MulDiv(12, monitorDpiY, 96);

to: Y = monitorInfo.rcWork.top + 50 + MulDiv(12, monitorDpiY, 96);

Line 1244: Y = rc.top;

to: Y = rc.top + 50;

Line 1285: Y = monitorInfo.rcWork.top;

to: Y = monitorInfo.rcWork.top + 50;

Line 1335: Y = monitorInfo.rcWork.top;

to: Y = monitorInfo.rcWork.top + 50;

(THE LINE NUMBERS MIGHT HAVE CHANGED DUE TO VERSION OF THE MODD! Above is for v1.1.2)

In ToolbarForWindows11 settings you must then specify how much space should be given to the Windows 11 taskbar, by default The settings are 80 pixels.


