# Python Script to Application

**To create an (.exe) executable application file from a python script**.


<!-- Badge section -->

[![Documentation](https://img.shields.io/badge/Documentation-blue)](README.md)
[![Languages](https://img.shields.io/badge/Python-FFD43B?plastic&logo=python&logoColor=blue)](https://www.python.org/)
[![OS](https://img.shields.io/badge/Windows-0078D6?style=plastic&logo=windows&logoColor=white)](README.md)



## Steps :

1. Install **[Inno Setup Compiler](tools/innosetup-6.1.2.exe)** free application and Pyinstaller. </br>
   - Your computer must be running Python3 or newer.
  
   Open **windows shell** and run :
   
```
pip install pyinstaller 
```
2. Save Python script with all the resources in one folder.

3. Open folder and press 'Shift + right click' select **Open PowerShell window**.</br> 
  
   Run below commands:

* If no custom icon file were used.

```
pyinstaller myprogram.py
```

* With custom icon file **(-F -i " " command)**.
   
```
pyinstaller -F -i "mylogo.ico" myprogram.py
```
   - ( mylogo.ico = icon file name, myprogram.py = Python file name )
   
   
   
* If you want your executable application in one file `--onefile` and no console running `--noconsole` behind your application then go with the below line. If your app requires Windows Administrator permission then use `--uac-admin` command
  
```
pyinstaller -F -i "mylogo.ico" myprogram.py --onefile --noconsole
```
                                                        
* If you want your executable application with additional file `--add-data` command, then go with the below line.
  
```
pyinstaller -F -i "mylogo.ico"--add-data "Additionalimage.png;." myprogram.py --onefile --noconsole
```

4. Go to **dist** folder and get application file, delete remain file except for resources. </br>You successfully created your standalone application.</br>
 


* However if you want your application (.exe) as setup file, windows installer will extract the installation resources from itself and manage their installation directly then, go with the below steps.</br>


5. Open Inno setup to make (.exe) file which is Installable/Executable in PC, select create a new script file using **Script Wizard** and browse to select your application.</br>


6.  Select all required things for your application such as Icon of setup file, Before installation document, Licence .etc</br>

   
7. Click  **Yes** to all, in the end go to Output Folder get **setup file**  of application and click on open to install.</br>
  
   
   **You're done !**


## Precautions :
1. Save the resources in one folder, Do not save the folder inside another folder

   - It will not give full permission to execute the commands.</br> #        ParentContainsErrorRecordException


2. Check Spellings before running the commands, Do not put any _space_ in your main python (.py) programme file name.

   - File not found show

3. Do not use the _icon_ word as a name of your icon (.ico) file, always use a different name.

   - It will show no 'icon file found'

4. Do not Close Powershell window until **Building EXE from EXE-00.toc completed successfully** 
Message not shows.</br>

### Refrences
* [Pyinstaller](https://pyinstaller.readthedocs.io/en/stable/operating-mode.html)
* [Inno Setup Compiler](https://jrsoftware.org/isdl.php)</br>
* [Real Python](https://realpython.com/pyinstaller-python/#:~:text=PyInstaller%20supports%20making%20executables%20for,machine%20for%20each%20supported%20OS)

Feel free to report <b>[issues](https://github.com/Abhijeetbyte/Python-Script-to-Application/issues/new)</b>




     
 
