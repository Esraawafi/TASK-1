#   Installation
For Installation we need to download VirtualBox and Ubuntu 20.04.4 LTS

* https://www.virtualbox.org/
* https://releases.ubuntu.com/20.04/

then install ROS Noetic package on  Ubuntu 
here the step of Installation


#   1.  Setup your sources.list
Setup your computer to accept software from packages.ros.org.



**`sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'`**



# 2. Set up your keys

**`sudo apt install curl # if you haven't already installed curl`**
**`curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -`**



# 3. Installation

First, make sure your Debian package index is up-to-date:

sudo apt update

![‏‏لقطة الشاشة (246)](https://user-images.githubusercontent.com/110434554/182726056-97e7de57-ce9c-4448-8487-0bd37700fcfc.png)


Now pick how much of ROS you would like to install.

**Desktop-Full Install**: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages

**`sudo apt install ros-noetic-desktop-full`**


**Desktop Install**: Everything in ROS-Base plus tools like rqt and rviz

**`sudo apt install ros-noetic-desktop`**


![‏‏لقطة الشاشة (249)](https://user-images.githubusercontent.com/110434554/182726152-44886fb4-d8e4-41fa-9ade-f3509a04cdb0.png)


**ROS-Base**: (Bare Bones) ROS packaging, build, and communication libraries. No GUI tools.

**`sudo apt install ros-noetic-ros-base`**


There are even more packages available in ROS. You can always install a specific package directly.

**`sudo apt install ros-noetic-PACKAGE`**
e.g.
**`sudo apt install ros-noetic-slam-gmapping`**

To find available packages, see ROS Index or use:

**`apt search ros-noetic`**

# 4. Environment setup
You must source this script in every bash terminal you use ROS in.

**`source /opt/ros/noetic/setup.bash`**

It can be convenient to automatically source this script every time a new shell is launched. These commands will do that for you.


If you have more than one ROS distribution installed, ~/.bashrc must only source the setup.bash for the version you are currently using.

Bash

**`echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc`**
**`source ~/.bashrc`**


zsh

**`echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc`**
**`source ~/.zshrc`**

# 5. Dependencies for building packages
Up to now you have installed what you need to run the core ROS packages. To create and manage your own ROS workspaces, there are various tools and requirements that are distributed separately. For example, rosinstall is a frequently used command-line tool that enables you to easily download many source trees for ROS packages with one command.

To install this tool and other dependencies for building ROS packages, run:

**`sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential`**

![‏‏لقطة الشاشة (252)](https://user-images.githubusercontent.com/110434554/182726265-3fd3164a-fa1c-44d5-9ce8-85a6c97864d1.png)

**Initialize rosdep**

Before you can use many ROS tools, you will need to initialize rosdep. rosdep enables you to easily install system dependencies for source you want to compile and is required to run some core components in ROS. If you have not yet installed rosdep, do so as follows.

**`sudo apt install python3-rosdep`**

With the following, you can initialize rosdep.

**`sudo rosdep init`**
**`rosdep update`**

![‏‏لقطة الشاشة (253)](https://user-images.githubusercontent.com/110434554/182726338-22c73fd2-db8c-44e2-9fe7-f4788bce7fd1.png)


**roscore **

to see if the packages is install  and have his own path 

![‏‏لقطة الشاشة (245)](https://user-images.githubusercontent.com/110434554/182725395-80166870-7781-4abc-a2dd-8e6f3c9124a2.png)

