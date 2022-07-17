# ROS-INSTALLATION
1- first we will download VirtualBox from here https://www.virtualbox.org/wiki/Downloads

2-we will go to the ubuntu page to download ubuntu , I downloaded version 20.04 , then choose ubuntu for desktop

3-Now you need to set up the virtual box to create your virtual machine: by clicking on New > and choosing a name for the virtual machine, make sure that the type is Linux and the size is 46 bits, and then press the continue button

4-For choosing the memory size, it is recommended to choose 1024 MB

5-Then, when creating the hard disk, choose the second option using Create virtual hard disk now

6-The file type must be the hard disk VDI (VirtualBox Disk Image)

7-For physical hard disk storage: dynamically allocated

8-In this step, you will set the storage for the device to 35 GB - 10 GB is recommended but it is very little because Ubuntu requires 25 GB at most

9-After creating your virtual device, now go to Virtual-Box and press the green arrow to start

10- A window will appear, click on the small file on the right, then you want to navigate where you have stored your Ubuntu file, press open and then start

11- It will take you directly to the setup process, which may take a few minutes

12- It will take you to a small welcome screen, make sure you choose your preferred language correctly and then click Install Ubuntu, choose the keyboard language you prefer

13- For updates and other software, choose normal installation and for the other option select Download updates while installing Ubuntu

14- Then choose the type of installation: scan disk and install ubuntu (don't worry about the warning because it is not using the host machine, it is using the virtual disk) .. then press the install now button

15 - Configuration window will pop up, just press Continue

16- Choose your time zone, and create your computer account

17- It will take you to the installation process, and it will take some time to complete

18- After the installation is complete you need to restart the virtual machine

19- Once again the error messages will appear, don't worry about them, they will disappear in a second

20-Hit the enter key, set up on top of your tweaks and then you're ready to go with Ubuntu

                     Next steps to install Rose on Ubuntu
1-Unlock your device on your virtual device

2-Type this command line to configure your source

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

3-You need to enter the password you set for your virtual computer

4-Next you need to prepare your keys with this mother

sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

5-Before installing, you must first make sure that your Debian package index is up to date

sudo apt update

6-Now you will install Rose through the following command line

7- You need to prepare your environment now
sudo apt install ros-noetic-desktop-full source /opt/ros/noetic/setup.bash

8- echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

9-source ~/.bashrc

10- rosversion -d

11-rosversion ros

12- rosversion -d

Through the following commands, you will control your virtual environment
1-printenv | grep ROS
2-rosversion -h 
3-To create a workspace for the rose mkdir -p ~/catkin_ws/src cd ~/catkin_ws/ catkin_make 
4-source devel/setup.bash 
5-To make sure you overlay your workspace correctly echo $ROS_PACKAGE_PATH /home/youruser/catkin_ws/src:/opt/ros/kinetic/share
