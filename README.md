# HapagVenture
Learn how to install and run the game! 

This README is a short walkthrough of how to get HapagVenture running. It is only for the **Windows OS**.

<hr/>

## System Requirements
1. Python
    
    <strong>Minimum System Requirements</strong>

    - Processors: x86 64-bit CPU (Intel / AMD architecture)
    - Disk space: 5 GB
    - Operating systems: Windows* 7 or later
    - Python* versions: 3.11.3 (Latest release)
    - RAM: 4 GB RAM


2. MySQL

    <strong>Minimum Hardware Requirements</strong>
    
    - CPU: Intel Core or Xeon 3GHz (or Dual Core 2GHz) or equal AMD CPU
    - Cores: Single (Dual/Quad Core is recommended)
    - RAM: 4 GB (6 GB recommended)
    - Graphic Accelerators: nVidia or ATI with support of OpenGL 1.5 or higher
    - Display Resolution: 1280×1024 is recommended, 1024×768 is minimum.
    
    <strong>General Requirements</strong>
    
    - The Microsoft .NET 3.5 Framework.
    - Cairo 1.6.0 or later
    - glib-2.10
    - libxml-2.6
    - libsigc++ 2.0
    - pcre
    - libzip 
  
## Installing Python
 - Simply go to https://www.python.org/downloads/ and install the latest version.
    - Make sure to select the option "Add python.exe to PATH" and simply click on "Install Now"
    ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/1.PNG?raw=true)
    
 <hr/>
 
 ### Installing python modules
 Enter these commands in cmd
  - Upgrade pip (If applicable)
   > py -m pip install --upgrade pip
  - Install Pygame
   > py -m pip install pygame
  - Install pandas
  > py -m install pandas
  - Pygame text input
  > py -m pip install pygame-textinput
  - Install MySQL onnector
   > py -m pip install mysql-connector-python
 
 ## Installing MySQL
 **NOTE: The steps mentioned over here are implemented with the aim of running the game locally. Feel free to experiment with the steps for your requirements.**
 - Simply go to https://dev.mysql.com/downloads/windows/installer/8.0.html and install the **mysql-installer-community-8.0.33.0.msi** version.
    - Chose Developer Default
    ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/2.PNG?raw=true)
    - After executing the required installations, chose **Development Computer** as the Config type
    ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/3.PNG?raw=true)
    - Next click on Add Users. The following settings are enough to get our game running.
    ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/4.PNG?raw=true)
    ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/5.PNG?raw=true)
    - Execute the configuration steps
    - You don't need to do anything with the MySQL Router Configuration
    - Enter root password
    ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/6.PNG?raw=true)
    
 - After the installation has been completed, you should be presented with a window as shown below
 ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/7.PNG?raw=true)
 - You have two options from here on out
    1. Use the root account for creating the database
        - Simply click on **Local instance MySQL80** and enter the root password
    2. Create a connection with the user account you have added in the earlier steps
        - Click on the + icon <br/>
        ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/8.PNG?raw=true)
        - Enter the username and click on Test connection. You will be prompted to add the password for the user
        ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/9.PNG?raw=true)
        - If the test is successful you will be presented with the following window. Click on the new MySQL connection created.
        ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/10.PNG?raw=true)
        
    Both the steps will lead you to the same window. Simply add the following code and execute the commands with **Ctrl+Shift+Enter**.
    ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/11.PNG?raw=true)
    > CREATE DATABASE hapaggame;
    
    > USE hapaggame;
    
    > CREATE TABLE customers (Name varchar(50), Company varchar(50), Q1 int, Q2 int, Q3 int, Q4 int, Q5 int, Q6 int, Q7 int, Q8 int, Q9 int, Q10 int, Q11 int, Q12 int, Q13 int, Q14 int, Q15 int);

 Congratulations! You have your database ready.
 
 ## Working on the Python files
 You can open the Python IDLE. Go to **File -> Open -> [File Name]**.
 ### Connecting MySQL database with Python
 - In the files **End_Screen.py** and **MySQLPrint_CustomerInfo.py**, make sure the following code has the correct information.
 ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/12.PNG?raw=true)

### Final touches
- In the following files, change the file path of certain variables to the one in your system. (You can simply use Ctrl+H to replace the text)   
    - Main.py, mainMenu.py, AnimatedIntro.py, decorations.py, Enemy.py, game_data.py, level.py, overworld.py, particles.py, Player.py, Quiz.py, ui.py, End_Screen.py
- Press **Ctrl+F5/Run -> Run Module** to run the file Main.py

### Viewing information in Excel
- Ensure that there is a file named **CustomerData** in the same directory as your python files
- Close the excel document if open. Run the file **MySQLPrint_CustomerInfo.py**. Now you can view the customer data.

### Converting the game into an executable (optional)
- In cmd, go to the directory where Main.py is located. Run the following commands
> py -m pip install pyinstaller

> pyinstaller --noconsole Main.py

- Copy paste the following files from the folder ..\Code2 to ..\dist\Main
    - ARCADEPI.ttf, Fipps-Regular.otf, ps4_keys.json
- You will see an executable file in ..\dist\Main called **Main.py**. Click on it to run the game.
    ![image](https://github.com/Y0SH1J/HapagVenture/blob/main/13.PNG?raw=true)
 
<hr/>

# And we are done! Enjoy the game :) 
## Note: This is a prototype for the game. It is not optimized.
