  
  
  
  
  
  
[DOWNLOADS](#)[STORE](#)[CONTACT US](#)  
  
  
  
  
  
  

Eugene Updater

[go back to support
                home](EN_EUGENE_HOME.md)  

![image](../images/Eugene/Eugene250.png)
  
  
  

[Eugene Basics  

              ](EN_EUGENE_ABOUT.md)

[Adaptronic
                Logviewer  

              ](EN_EUGENE_LOGVIEWER.md)

[  

              ](EN_SelFW.md)

  

  
  
  
  
  
  
[Description
                    and Operation](EN_EUGENE_UPDATER.html#I._Description_and_Operation)  
[Features](EN_EUGENE_UPDATER.html#II._Features)  
[Troubleshooting](EN_EUGENE_UPDATER.html#III._TroubleshootingFAQ)  
  
[]()Description and Operation  
  
  
The Updater tool downloads
                  file updates and new files like firmware and help files. It
                  can do so automatically with a user set interval (default =
                  12hrs)  or manually, triggered from the updater itself or
                  Eugene. When an update is triggered, the Updater will download
                  a list of files from the server. If the file in the list
                  exists but not locally, it is downloaded. If the local file is
                  older than the one in the list, it is downloaded as well.
                  The file gets downloaded to the
                  <Username>\Documents\Eugene\Updates folder.  
  
After download, the local file is deleted (if it exists), and
                  moved to the folder where the Updater is (EugeneUpdate.exe),
                  which is the Eugene installation folder. The updater then
                  moves on to the next file in the list. A special case
                  exists for Eugene.exe and Logviewer.exe. If one of these
                  programs (for example, Eugene) are open, the updater will move
                  the file anyway and the user is prompted that an update
                  exists. Should you choose to update, UpdateKicker.exe will
                  close the program, delete the old one and rename the updated
                  file  (for example, Eugene.ex_ to Eugene.exe).  
  
All operations are logged for easier diagnostics.  
[]()Features  
  
  
The updater window when no
                  update is being downloaded. Clicking on the "play" button will
                  trigger an update check, regardless of the update check mode
                  (auto or manual).  
  

![default window](../images/Eugene/Updater_1.png)
  
The Options Menu.  
[
![Updater options](../images/Eugene/Updater_2.png)
](EN_EUGENE_UPDATER.md)  

- Sets Auto Update mode.
- Sets auto update check interval.
- Enabling this will generate a more detailed log of
                      the update. It will include the list of files in the
                      update and the reason why a file is added to the
                      "download" list.
- Toggles the registry entry to auto-run on Windows
                      launch.  
The Actions Menu.  
[
![Updater Actions](../images/Eugene/Updater_3.png)
](EN_EUGENE_UPDATER.md)  

- Same function as the "play" button.
- Views the logfile. The option will be disabled when
                      an update is in progress as the updater is writing into
                      the logfile at this time.
- Deletes all the files in the catcher folder
                      (<Username>\Documents\Eugene\Updates).The updater window can be accessed via the Windows System
                  Tray icon (bottom right). If the updater is running, it should
                  appear here. Also, this is a good way to check if the updater
                  is launching on Windows start-up or not.  
  
[
![system tray](../images/Eugene/Updater_4.png)
](EN_EUGENE_UPDATER.md)  
  
Right clicking on the icon will show a menu that contains the
                  common operations that can be done thru the main window. This
                  allows easier configuration without having to access the main
                  window itself.  
  
[
![popup menu](../images/Eugene/Updater_5.png)
](EN_EUGENE_UPDATER.md)  
  
[]()Troubleshooting/FAQ  

- My updater is not
                      running on startup.  
  
First, launch the updater
                  from the start menu, under "Adaptronic Engine Management".
                  Check the icon in the Windows system tray and make sure the
                  "Launch on system startup option is checked.  
  
If this still does not work, you'll have to check the registry
                  entry. Press the Windows Button + R, type regedit.exe into the
                  window that appears. Browse into
                  HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run
                  or simply paste
                  "Computer\HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run"
                  into the address bar. There should be a EugeneUpdater entry
                  there, with value set to the path of EugeneUpdater.exe. The
                  value should be a string. The path shown in the image is the
                  default path.  
  
[
![registry](../images/Eugene/Updater_6.png)
](EN_EUGENE_UPDATER.md)  
  
  
Restart your computer to
                  check if the process worked. Otherwise, send us an email at
                  tech@adaptronic.com.au.  
  

- My updater fails to
                      get any updates (or any download failure).  
First, try to access this
                  link. It should download the file. This is the "list" file
                  mentioned earlier.  
  
[https://s3.amazonaws.com/](https://s3.amazonaws.com/adaptronicupdaterfiles/Update.info)[adaptronicupdaterfiles/Update.](https://s3.amazonaws.com/adaptronicupdaterfiles/Update.info)[info](https://s3.amazonaws.com/adaptronicupdaterfiles/Update.info)  
  
If it does not download, there might be a problem with your
                  connection or the connection to the server, in which case, try
                  updating again at a later time.  
  
If it does, then it might be blocked (as a false
                  positive) by the antivirus or antimalware installed in your
                  system. All of these have the ability to add exclusions,
                  either a file or the whole folder. We recommend excluding the
                  whole folder if the option is available. The default path (if
                  you did not change it in the installation process) is
                  C:\Adaptronic Engine Management\Eugene. If you can only
                  exclude files, exclude EugeneUpdater.exe.  
  
Here is an example of adding an exclusion into Norton 360:  
[
![exclusion_norton](../images/Eugene/Updater_7.png)
](EN_EUGENE_UPDATER.md)  
  
  
Why
                    is the update being blocked in the first place?  
  
  
By
                  design the updater downloads individual files, which includes
                  exes. We used to download the exe as it is, but now we
                  download these files in a different filename, then renamed
                  locally. In the future we might opt to download the files as
                  an archive then deploy. This should be a good middle ground
                  vs. letting the update download an installer which kind of
                  defeats the purpose of the updater.  
  

- My updater keeps on
                      downloading files, and the same files every time.  
First, try to purge the
                  update folder (Actions -> Purge Update folder), and check
                  your system time. The updater's decision to download an
                  existing file or not is determined largely by the system time.  
  
Failing that, enable "Verbose reports", try an update and send
                  log_download.txt to us at tech@adaptronic.com.au. It is
                  located by default in C:\Adaptronic Engine Management\Eugene.
                  It is of importance to us as there might have been an error in
                  the file naming or dates of the files uploaded.  
  
Also kindly send us a log if a specific file does not get
                  downloaded and updated and if the others do. This points to an
                  internal remote file naming issue, which should be reported to
                  us immediately.  
[Back to top](EN_EUGENE_UPDATER.html#top)  
  
©2018
        Adaptronic  
  
