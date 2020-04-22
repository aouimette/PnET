# Getting setup to run PnET on Windows10

### Install a code editor or IDE
Currently, PnET is written in C++. To work with the PnET code we will want some sort of `code editor` or `integrated development environment (IDE)`. A good choice is [Visual Studio Code](https://code.visualstudio.com/download), which as a C/C++ extension. Find and download this extension in VSCode in the Extension View.  First press (Ctrl+Shift+X) to get into Extension View, then in the search field type C/C++.  You should see the C/C++ option under the search field.  Click on it and it should appear in the main window.  Click the "install" button for the C/C++ extension in the main window.

### Install MinGW
At the very least, we need a `compiler` to convert *human-readable* source code into *computer-executable* machine code. For Windows, a common choice is a version of [MinGW](https://en.wikipedia.org/wiki/MinGW) called Mingw-w64. 

*Note that here we are following along with a [VScode setup tutoral](https://code.visualstudio.com/docs/cpp/config-mingw).*
1. Go to [SOURCEFORGE](https://sourceforge.net/projects/mingw-w64/). Click `Files`, scroll down to "MinGW-W64 Online Installer" and download `MinGW-W64-install.exe`
2. Run the installation file, and select the default settings. Pay attention to where the files are installed -- likely program files.
3. Add MinGW `bin` to the PATH environment
+ Type `settings` into the Windows search bar
+ Search for `Edit environmental variables for your account`
+ Double-click `Path`
+ Click `New`, then `Browse...`, and navigate to where you downloaded MinGW. The path will depend on where you've put the files, but it will look something like: `C:\Program Files (x86)\mingw-w64\i686-8.1.0-posix-dwarf-rt_v6-rev0\mingw32\bin`
+ Add this path, and click `OK`. 
4. Check MinGW installation by opening the Command Prompt and typing:
    `g++ --version`
     and
    `gdb --version`.
    If these commands aren't recognized or you don't get an expected output, doublecheck the Path environment settings.
