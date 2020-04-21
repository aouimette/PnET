# Getting setup to run PnET on Windows10

Currently, PnET is written in C++. To work with the PnET code we will want to use some sort of code editor or integrated development environment. A good choice is [Visual Studio Code](https://code.visualstudio.com/download), which as a C/C++ extension. Find and download this extension in VSCode in the Extension View (Ctrl+Shift+X).

At the very least, we need a `compiler` to convert *human-readable* source code into *computer-executable* machine code. For Windows, a common choice is a version of [MinGW](https://en.wikipedia.org/wiki/MinGW) called Mingw-w64. 

### Install MinGW
*Note that here we are following along with a [VScode setup tutoral](https://code.visualstudio.com/docs/cpp/config-mingw).*
1. Go to [SOURCEFORGE](https://sourceforge.net/projects/mingw-w64/), and click the download button.
2. Add MinGW `bin` to the PATH environment
+ Type `settings` into the Windows search bar
+ Search for `Edit environmental variables for your account`
+ Double-click `Path`
+ Click `New`, then `Browse...`, and navigate to where you downloaded MinGW. The path will depend on where you've put the files, but it will look something like: `C:\Program Files (x86)\mingw-w64\i686-8.1.0-posix-dwarf-rt_v6-rev0\mingw32\bin`
+ Add this path, and click `OK`. 
3. Check MinGW installation by opening the Command Prompt and typing:

>>`g++ --version`

>>`gdb --version`

>>If the command isn't recognized or you don't get an expected output doublecheck the Path environment settings.
