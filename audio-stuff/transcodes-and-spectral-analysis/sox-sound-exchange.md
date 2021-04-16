---
description: for Windows. Instructions written by newstarshipsmell.
---

# SoX \(Sound eXchange\)

Go to [https://sourceforge.net/projects/sox/files/sox/14.4.2/](https://sourceforge.net/projects/sox/files/sox/14.4.2/)

Download either the installer \(**sox-14.4.2-win32.exe**\) or portable \(**sox-14.4.2-win32.zip**\) version.

If you choose to install it, rather than using the portable version, you must change the default installation folder to somewhere besides **C:\Program Files** / **C:\Program Files \(x86\)** - otherwise, Windows permissions will prevent SoX from creating the output image files.

![](../../.gitbook/assets/image%20%2854%29.png)

Install or unpack SoX to the desired location.

Once you've installed or unpacked it, open Notepad and paste the following text into it:

`c:  
cd %~dp0  
mkdir Spectrograms  
FOR %%A IN (%*) DO sox %%A -n remix 1 spectrogram -x 3000 -y 513 -z 120 -w Kaiser -o "Spectrograms\%%~nxA-full.png"  
FOR %%A IN (%*) DO sox %%A -n remix 1 spectrogram -X 500 -y 1025 -z 120 -w Kaiser -S 1:00 -d 0:02 -o "Spectrograms\%%~nxA-zoom.png"  
pause`

Save the file as **spectrograms.bat** inside the folder you just installed/unpacked SoX to. You're done!

