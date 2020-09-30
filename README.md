# SOP (Standard operating procedure)

This will guide you to the prerequisites, steps to run the application . before continuing I will state my assumptions.
 * the machine used is preconfigured with all the network andd DCOM settings.
 * the machine used has no version of python installed. if so then do check Faqs section.
 *if you get strucked att any point of time feel free to contact us*

## Pre requisites for Installing the software 
There are cretain prerequisites for the project to be able to run on the system.
 1. The machine on which we are trying to run the program needs to be checked if it can connect to a remote server (if using a laptop to connect in the network's server ) using any tool of the prefrence such as the matrikon client.
 1. If the above step does seem to work we can go ahead for the installation.
 1. The softwares we need to make sure the application run on your machine correctly are as follows : 
      * [python3.6.8](https://www.python.org/ftp/python/3.6.8/python-3.6.8.exe) 32 bit version
      * [Pywin32](https://github.com/mhammond/pywin32/releases/download/b228/pywin32-228.win32-py3.6.exe) Package 
      * [qt4](https://download.qt.io/archive/qt/4.8/4.8.7/qt-opensource-windows-x86-vs2010-4.8.7.exe) package 
      * OPC DA COM component is [opcdaauto.dll](http://gray-box.net/files/graybox_opc_automation_wrapper.zip) x86 version.(I am refering the folders in the package  here )
note :*all the packages above mentioned contains a link in it which can be used to download the softwares or at the section end we will share the bundled package too so that you may not need get them seprately this section is just here to ensure that due to any restriction the process may not stop.*

1. if you get all the required softwarers successfully lets install them one by one with a procedure so that yoou may not fail at any step 
   1. install python and dont forget to check "ADD TO PATH " option. that`s manadatory.
      open a command window and check that we have installed the python correctly.
      ```cmd     
       C:\users\Yourusername>python --version
       Python 3.6.8
       ```
       
      if you see similar output then you have successfully installed the python. 
   1. install the pywin32 package now.
   1. install the qt4 package (the largest one aprrox 230MB).
   1. register the dll with the below steps
     1. extract the graybox_opc_automation_wrapper.zip
     1. head to x86 folder. 
     1.open an elevated command window (i.e right click and run as administartor) and run the below command
     
        ```cmd C:\users\Yourusername>regsvr32 ```
    1. hope you have seen a windows saying the dlll registered successfully.
 *now we have installed all the required packages so head toward running the application step by step*
 
## steps to run the application 

 To run the provided application. first download it from [here](https://drive.google.com/file/d/1QAY6qECmUW8D19BVNAGfhhIZn8oudRpY/view?usp=sharing). and then follow the steps below:
  1. extract the zip to a folder in desktop know as opc_work.
  1. open the opc_work then app and open a command window with the working directory as the directed one.
  1. run the below command 
  
    ```cmd  c:\users\Yourusername\Desktop\opc_work\app>python gui.py```
  1. now you will be asked for a prompt where you can configure the servers`ip to start the gui to work with.here in the prompt respond as stated
      if the machine is same where the opc server is installed ,then just press enter else enter the ip of the machine where the opc server is installed
  1. if you got the gui you are good to start the logging of the data .but if you dont get it just read the instructions carefully 
   rest will be illustrated using the screenshots below 
 
    
