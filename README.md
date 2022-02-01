# Python-Script-to-Application

To create an .exe [application] file from a python script 


  # Precautions :

                
   * Save the resources in one folder, Do not save the folder inside another folder [ It will not give full
     
     permission to execute the commands. # ParentContainsErrorRecordException]
  
   * Check Spellings Before Running the commands, Do not put any Space in your main python programme Name. [# File not found show]
   
   * Do not use the " icon " word as a name of yours. ICO [icon] file; always use a different name. [ # It will show no icon file found]
   
   * Do not Close Powershell window until "Building EXE from EXE-00.toc completed successfully" Message not shows.     


  # Steps :


1. Install [Inno Setup Compiler](https://github.com/Abhijeetbyte/Python-Script-to-Application/raw/main/tools/innosetup-6.1.2.exe) free application and Pyinstaller.

   Run this line-> 
   
 *                                pip install pyinstaller   

2. Create an .ICO [icon ] file, Save Python script with all the resources in the same folder.

3. Open folder and press 'Shift + right click' select and run 'Open PowerShell window'

   Run this line-> 
   
 *                                pyinstaller -F -i "myicon.ico" myscriptname.py


 * [ myicon.ico = icon file name  myscriptname.py = Python file name ]
   
   
3. 1 if you want your executable application with no console running  behind your
     application then go with the below line 
  
 *                                pyinstaller -F -i "myicon.ico" myscriptname.py --onefile --noconsole
 *                                
                                 
3. 2 if you want your executable application with additional file (--add-data command) and no console running  behind your
     application then go with the below line 
  
 *                  pyinstaller -F -i "myicon.ico"--add-data "AdditionalImage.png;." myscriptname.py --noconsole                           

4. Go to " dist " folder and get application file, delete remain file except for resources.

5. Open Inno setup to make .exe file which is Installable /Executable in Windows PC, select ‘ Create a new script file using script       
   Wizard ' and browse to select your application. 

6. Select all required things for your application # Icon of setup file # Before installation document # Licence .etc 
   
7. Click  ' Yes ' to all, in the End, go to Output Folder get 'setup file'  of application and click on open  to install.

