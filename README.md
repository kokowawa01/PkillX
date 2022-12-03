# PkillX
A small graphical program that closes any program on the GNU Linux system, by writing the name of the program, and it can also be used through the terminal.

First, make sure that the installed distribution on your device contains the GTK version 2.24, or 3, or 4 libraries.

Second, go to the source folder and type the following commands:

gcc -c dialog.c `pkg-config --libs --cflags gtk+-3.0`

gcc -shared dialog.o -o libpkillx.so `pkg-config --libs --cflags gtk+-3.0`

sudo cp -av libpkillx.so /usr/lib/

gcc pkillx.c /usr/lib/libpkillx.so -o pkillx `pkg-config --libs --cflags gtk+-3.0`

