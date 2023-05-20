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
    ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/8c7fa330-6b5c-494c-81a6-b2754cd0a406)
    
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
    ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/389bc333-a8f6-4de5-a7cd-02c47c589180)
    - After executing the required installations, chose **Development Computer** as the Config type
    ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/7131d118-7ccc-4805-b8d9-8b68a603852b)
    - In Account and Roles, set your root account password.
    - Next click on Add Users. The following settings are enough to get our game running.
    ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/f55e7f4c-eeb6-4359-8c33-58f056ac2cdd)
    ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/b2af331a-0ca6-4975-9e60-7acea3e39d45)
    - Execute the configuration steps
    - You don't need to do anything with the MySQL Router Configuration
    - Enter root password
    ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/08cd01d3-5a91-4478-9c19-cc524816c99d)
    
 - After the installation has been completed, you should be presented with a window as shown below
 ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/86f1608b-f584-4750-b262-b0e3d4290140)
 - You have two options from here on out
    1. Use the root account for creating the database
        - Simply click on **Local instance MySQL80** and enter the root password
    2. Create a connection with the user account you have added in the earlier steps
        - Click on the + icon <br/>
        ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/d72fca1b-5219-4f09-855c-53e7474e190c)
        - Enter the username and click on Test connection. You will be prompted to add the password for the user
        ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/df66c063-4f19-4b2b-8a63-6e36dfe55a72)
        - If the test is successful you will be presented with the following window. Click on the new MySQL connection created.
        ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/546d12fd-ca25-4b36-a436-921f17eacad6)
        
    Both the steps will lead you to the same window. Simply add the following code and execute the commands with **Ctrl+Shift+Enter**.
    ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/9fc26170-da37-42fb-af6c-ac15b7945a90)
    > CREATE DATABASE hapaggame;
    
    > USE hapaggame;
    
    > CREATE TABLE customers (Name varchar(50), Company varchar(50), Q1 int, Q2 int, Q3 int, Q4 int, Q5 int, Q6 int, Q7 int, Q8 int, Q9 int, Q10 int, Q11 int, Q12 int, Q13 int, Q14 int, Q15 int);

 Congratulations! You have your database ready.
 
 ## Connecting MySQL database with Python
 - In the files **End_Screen.py** and **MySQLPrint_CustomerInfo**, make sure the following code has the correct information.
 ![image](https://github.com/Y0SH1J/HapagVenture/assets/122041317/20c96358-375d-4c13-8814-eff7a8e3b7cd)

## Final touches
- In the following files, change the file path of certain variables to the one in your system. (You can simply use Ctrl+H to replace the text)   
    - Main.py, mainMenu.py, AnimatedIntro.py, decorations.py, Enemy.py, game_data.py, level.py, overworld.py, particles.py, Player.py, Quiz.py, ui.py, End_Screen.py

<hr/>

# And we are done! Enjoy the game :) 

