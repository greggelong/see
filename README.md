# see
## a place to put some C code

Now I see why you need gitignore!

I haven't really had compiled and executable files

in the same directory as I was using python and javaScript

but you really need that gitignore if you are compiling.

making all the .o and .exe 


## setting up vs code on windows 10 

had some trouble setting up vs code to compile and run

c programs.

I had already downloaded codeblocks and could easily compile

as well as being able to compile and run in the linux sub system

But I was not able to get vs code to find the path to codeblocks compiler.

so in the end I had to install minGW and add the path 

I followed instructions from vscode help.

https://code.visualstudio.com/docs/languages/cpp

and it actually worked.

this video was also helpful

to walking through the configure process

https://youtu.be/77v-Poud_io

## Cloned onto my raspberry pi

I wanted to also use my raspberry pi.

However my pi has very limited memory and I wanted to work off

the usb drive I am using for downloads.

However I could not change the permissions to executable

with chmod +x  

it seems my pi usb is fat format

I will need to format a different drive 

or mount this one differently


https://askubuntu.com/questions/499275/how-to-set-usb-drive-with-executable-permission


## update I got the permissions changed 


Making the USB disk on the Raspberry Pi have permission for executables.

Which you need to run compiled c files.

My disk is mounted in sda1

I had already made a folder in media called media/gregUsb

I mount the usb to that

pi@raspberrypi:~ $ sudo umount /dev/sda1

 
pi@raspberrypi:~ $ sudo mount -t vfat -o rw,exec,uid=1000,gid=1000,umask=022 /dev/sda1 /media/gregUsb
 
pi@raspberrypi:~ $ cd /media/gregUsb

you can navigate using the terminal 

from the gui file system the name will still look like the name of the USB eg. Kingston

but if you open a terminal there it will open to media/gregUsb

then to unmount 


pi@raspberrypi:~ $ sudo umount /media/gregUsb
