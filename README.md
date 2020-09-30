# SOP (Standard operating procedure)

This will guide you to the prerequisites, steps to run the application . before continuing I will state my assumptions.
 * the machine used is preconfigured with all the network and DCOM settings.
 * the machine used has no version of python installed. if so then do check Faqs section.
 
 
 *if you get strucked at any point of time feel free to contact us*

## Pre requisites for Installing the software 
There are cretain prerequisites for the project to be able to run on the system.
 1. The machine on which we are trying to run the program needs to be checked if it can connect to a remote server (if using a laptop to connect in the network's server ) using any tool of the prefrence such as the matrikon client.
 1. If the above step does seem to work we can go ahead for the installation.
 1. The softwares we need to make sure the application run on your machine correctly are as follows : 
      * [python3.6.8](https://www.python.org/ftp/python/3.6.8/python-3.6.8.exe) 32 bit version
      * [Pywin32](https://github.com/mhammond/pywin32/releases/download/b228/pywin32-228.win32-py3.6.exe) Package 
      * [qt4](https://download.qt.io/archive/qt/4.8/4.8.7/qt-opensource-windows-x86-vs2010-4.8.7.exe) package 
      * OPC DA COM component is [opcdaauto.dll](http://gray-box.net/download_daawrapper.php?lang=en) x86 version.(I am refering the folders in the package  here )

note :*all the packages above mentioned contains a link in it which can be used to download the softwares or at the section end we will share the bundled package too so that you may not need get them seprately this section is just here to ensure that due to any restriction the process may not stop.*

1. if you get all the required softwarers successfully lets install them one by one with a procedure so that yoou may not fail at any step 
   1. install python and dont forget to check "ADD TO PATH " option. that\`s manadatory.
      open a command window and check that we have installed the python correctly.
      ```cmd     
       C:\users\Yourusername>python --version
       Python 3.6.8
       ```
       
      if you see similar output then you have successfully installed the python. 
   1. install the pywin32 package now.
   1. install the qt4 package (the largest one aprrox 230MB).
   1. register the dll with the below steps
      1. extract the graybox_opc_automation_wrapper.zip.
      1. head to x86 folder. 
      1.open an elevated command window (i.e right click and run as administartor) and run the below command.
     
         ```cmd 
         C:\users\Yourusername\path\to\x86>regsvr32 gbda_aut.dll 
         ```
      1. hope you have seen a windows saying the dlll registered successfully.
      
 *now we have installed all the required packages so head toward running the application step by step*
 
## steps to run the application 

 To run the provided application. first download it from [here](https://drive.google.com/file/d/1QAY6qECmUW8D19BVNAGfhhIZn8oudRpY/view?usp=sharing). and then follow the steps below:
  1. extract the zip to a folder in desktop know as opc_work.
  1. open the opc_work then app and open a command window with the working directory as the directed one.
  1. run the below commands :
     
     ```cmd
      C:\users\Yourusername\Desktop\opc_work\app>python -m pip install -r requirements.txt
       ```
  
      ```cmd
      C:\users\Yourusername\Desktop\opc_work\app>python gui.py
       ```
  1. now you will be asked for a prompt where you can configure the server\'s IP to start the gui to work with. in the prompt respond as stated
      if the machine is same where the opc server is installed ,then just press enter else enter the ip of the machine where the opc server is installed
  1. if you got the gui you are good to start the logging of the data .but if you dont get it just read the instructions carefully.
  1. now that you got the gui there you can select the server opc name from the drop-down and then click connect.
  1. there will be a tag list as soon as you connect to the server. select some tags or select all then just click start logging and you can now see that the dat      a from the opc servers will be shown their so you may start getting the data on your screen and same data is sent to the aws server.
  
  
  
 ## Faqs
 
  1. you don't get the correct output from the command python --version.
    
       you might get this for two reasons 1. another python version is installed 2. you might have forgot to tick the add to path option.  
       solution : 1. another python version is installed 
       if this is the case
        1. press start search for python3.6 32 bit then right click and select open file location.
        2. if you see the shortcuts as their type in the file manager you might need to right click one of them and select open file locartion again. 
        3. once you get to the directory where python is installed , you may see python.exe just create a copy of this in the same directory and rename the copy            file with the name python3 
        
        2. you might have forgot to tick the add to path option
           simply add the python installation location to path.
    
       
  
 
    
