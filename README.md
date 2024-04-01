# GEGL Noise in Motion plugin (wood and metal) 

Download  Gimp plugin here
https://github.com/LinuxBeaver/Noise_in_Motion_Gimp_plugin/releases

![image](https://github.com/LinuxBeaver/Noise_in_Motion_Gimp_plugin/assets/78667207/169f9ec6-9e96-4b57-94a8-7c6a3312536f)

![image](https://github.com/LinuxBeaver/Noise_in_Motion_Gimp_plugin/assets/78667207/1b46d8c8-2139-4ac6-bbb5-421b1f76d9c7)

## OS specific location to put GEGL Filter binaries 

**Windows**
C:\Users\USERNAME\AppData\Local\gegl-0.4\plug-ins
 
**Linux**
 /home/(USERNAME)/.local/share/gegl-0.4/plug-ins
 
 **Linux (Flatpak)**
 /home/(USERNAME)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins

![image](https://github.com/LinuxBeaver/GEGL-glossy-balloon-text-styling/assets/78667207/f15fb5eb-c8d7-4c08-bbac-97048864e657)


## Compiling and Installing
**Linux**

To compile and install you will need the GEGL header files (libgegl-dev on Debian based distributions or gegl on Arch Linux) and meson (meson on most distributions).

meson setup --buildtype=release build
ninja -C build


If you have an older version of gegl you may need to copy to ~/.local/share/gegl-0.3/plug-ins instead (on Ubuntu 18.04 for example).

**Windows**

The easiest way to compile this project on Windows is by using msys2. Download and install it from here: https://www.msys2.org/

Open a msys2 terminal with C:\msys64\mingw64.exe. Run the following to install required build dependencies:

pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl

Then build the same way you would on Linux:

meson setup --buildtype=release build
ninja -C build

