# COSC6280-Final-Project
Files used during the course of the final project for COSC6280 at Marquette University.

The four .dd files are the payloads placed into the RP Pico; they must be renamed payload.dd to function properly.  They were taken from various payloads listed in the payload library (https://github.com/hak5/usbrubberducky-payloads).
Some modifications were made to the payloads compared to their original:
 - the keyword DEFINE was removed (or otherwise rendered moot), and associated code was made to function without reliance on DEFINE
 - the PASSIVE_WINDOWS_DETECT function was removed due to not working (unknown if malfunction is the result of device limitations/differences or my own ignorance)
 - some code snippets meant to obfuscate the shell or prevent the user from interrupting the keystroke injection were removed
 - for tree.dd specifically, the "Invoke-RestMethod" at the end of the STRINGLN was altered to use the variable $filePath; originally, the method used the non-existant variable $fileContent
 - for tree.dd and ffcookies.dd, my DropBox access token was used where asked for; while I believe the access token only had a lifespan or 4 hours and thus would not work now, the token has been removed regardless

The directory PicoDuckyBuilder-main is almost a direct copy of a repository (https://github.com/ryo-yamada/PicoDuckyBuilder), with the only change being to line 117 of windows.py to allow copying of a directory despite the destination having a directory with the same name.  The README file within should still be accurate.

The keylogger.exe program was originally planned to be used during the project, but was eventually cut.  I have included it here for transparancy's sake; a directory named 'logs' must exist within the program's own directory for the keylogger to make logs.
