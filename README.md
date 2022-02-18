# Python-Script-to-Application

**To create an (.exe) executable application file from a python script**

## Precautions :
                
:heavy_check_mark: Save the resources in one folder, Do not save the folder inside another folder.
> *It will not give full permission to execute the commands. # ParentContainsErrorRecordException*
  
:heavy_check_mark: Check Spellings before running the commands, Do not put any _space_ in your main python (.py) programme file name.
> *File not found show*

:heavy_check_mark: Do not use the _icon_ word as a name of your icon (.ico) file, always use a different name.
> *It will show no icon file found.*
   
:heavy_check_mark: Do not Close Powershell window until **Building EXE from EXE-00.toc completed successfully** Message not shows.

## Steps :

1.Install **[Inno Setup Compiler](main/tools/innosetup-6.1.2.exe)** free application and Pyinstaller. </br>

 Open **windows shell** and run :
   
```
 pip install pyinstaller   
 
```
2. Save Python script with all the resources in one folder.

3. Open folder and press 'Shift + right click' select **Open PowerShell window**


Run below commnads:

* If no custom icon file were used.
```
pyinstaller myprogram.py
```

* With custom icon file **(-F -i "mylogo.ico" command)**
   
```
pyinstaller -F -i "mylogo.ico" myprogram.py

```
* ( mylogo.ico = icon file name, myprogram.py = Python file name )
   
   
* If you want your executable application with no console running **(--noconsole command)** behind your application then go with the below line
  
```
pyinstaller -F -i "mylogo.ico" myprogram.py --onefile --noconsole

```
                                                        
* If you want your executable application with additional file **(--add-data command)** then go with the below line.
  
```
pyinstaller -F -i "mylogo.ico"--add-data "Additionalimage.png;." myprogram.py --noconsole
```
4. Go to **dist** folder and get application file, delete remain file except for resources.</br>

**Congratulations ! 🤩 you successfully created your standalone application.**</br>

*However if you want your application as Setup.exe then windows installer will extract the installation resources from itself and manage their installation directly*.</br>

5. Open Inno setup to make (.exe) file which is Installable/Executable in Windows PC, select **Create a new script file using script     
   Wizard** and browse to select your application. 

6. Select all required things for your application such as Icon of setup file, Before installation document, Licence .etc 
   
7. Click  **Yes** to all, in the end, go to Output Folder get **setup file**  of application and click on open to install.</br>

**Yor're done !**</br>
### Refrences
* [Pyinstaller](https://pyinstaller.readthedocs.io/en/stable/operating-mode.html)
* [Inno Setup Compiler](https://jrsoftware.org/isdl.php)</br>
* Feel free to report <b>[issues](https://github.com/Abhijeetbyte/Volume-Calculator/issues/new)</b>
 
