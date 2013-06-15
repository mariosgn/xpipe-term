X|Pipe - Graphical Terminal Emulator
==========

X|Pipe is the attempt to merge a terminal emulator, a file manager and a launcher.
A video of the working prototype is available at [vimeo](https://vimeo.com/68400623/)

Source code and License
==========

In short: GPL.
The code is currently not available. There are too many bugs and the code is totally unstable. When all the basic features are ready, I will move my private git repo on github.

Features
==========

Basics terminal stuff:

* Vt100 escape codes: like xterm and rxvt. vvtest should be happy
* Run on openpty on linux or starting with an SSH connection. This means: Linux, Windows and Mac
* Xterm 256 color, and standard formatting
* Themable fonts and color

Other terminal enhancements
* Themable in QML
* OpenGl backend
* Multi threaded tabbed in single window or standard multi window with shared IO channel
* Text selections: standard and in block. No mouse needed.
* Url and filename handling

The magic

* Zsh and Fish Shell (and a little part of bash) have been extended to be more eye friendly. Any tab completion shows files, command and command options in a human way.
* All shell command can be trapped and shown graphicly: these extensions are in written in QML or C++ 
* A graphical launcher connected to the shell as a standard pipe. The entries in the launcher can come from locate, zeitgeist, bookmarks and other sources. These sources are pluginable in qml, javascript and python.
* Graphical "sendto". Files, list of files, clipboard content or any other shell output can be sent to "places". Again standard pipes have been extended in python (or C++): email, skype, social networks can be reached directly from the terminal.
* File manager mode: with a keypress it's possible to witch from the standard comnand line to the filemanager mode: it is possible to navigate the filesystem and work with files with the benefits of a modern graphical interface. Thumbnails and standard icons themes are supported.
* You will have the best prompt ever

Milestones
==========

* **Vttest passing:** all escape codes have to work
* **Vim and emacs test:** if they works... the else it's a piece of cake
* **Source code release**: the judgment day 
* **File manager:** navigate the file system, run commands, see thumbnails, run files with xdg-mime... a standard  file manager
* **Tab completion:** everything... files, commands and options
* **Custom handlers:** support for custom command handler and plugin system for python and javascript  
* **Start in SSH mode:** prompt for host and password (ssh keys and friends)
* **Windows and Mac support:** no idea if posix pty exists on mac. Windows will use only the ssh connection
* **Launcher and plugis:** Integration of launcher sources as locate, gtk-bookmarks and zeitgeist... dbus?
* **SendTo:** python plugins and standard external commands

