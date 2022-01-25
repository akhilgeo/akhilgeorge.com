---
title: 'How to: Install gcc on Windows'
layout: post-right-sidebar
categories:
- Windows
image: assets/images/post/gcc.jpg
---

GNU Compiler Collection or commonly known as gcc is a compiler used for r C, C++, Objective-C, and other programming languages. Setting up gcc in windows is a tedious task sometimes. below is a simple method to install gcc on windows 10 or 11.

1. Download [MinGW - Minimalist GNU for Windows](https://sourceforge.net/projects/mingw/) from Sourceforge.
2. After downloading run `mingw-get-setup.exe`.
3. In MinGW installation manager, Select `mingw32-gcc-g++` under Basic Setup. 
		![]({{ 'assets/images/post/gcc select.png' | relative_url }})
4. From the menu select Installation > Apply changes.
5. The program will download and install the components.
		![]({{ 'assets/images/post/gcc install.png' | relative_url }})
6. Once installation is completed you need to set up enviornment variables
7. From Windows start, search `Enviornment Variables`. ![]({{ 'assets/images/post/gcc env variables.jpg' | relative_url }})
8. Select Enviornment Variables under Advanced tab.
9. Select `Path` under System variables and click on edit.  ![]({{ 'assets/images/post/gcc bin.png' | relative_url }})
10. Add` C:\MinGW\bin` and save.![]({{ 'assets/images/post/gcc env variable edit.png' | relative_url }})
11. Now open Terminal or command prompt and check `gcc --version`.![]({{ 'assets/images/post/gcc version.jpg' | relative_url }})

If the command returns you the gcc version, then gcc is installed on your system and the paths are configured as expected.
