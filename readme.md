The project is based on the SOM tutorial from ai-junkie.com:
http://www.ai-junkie.com/ann/som/som1.html

This is a demonstration of a SOM (self-organizing map) working upon COLORS.
The SOM will attempt to group (clusterize) the colors just by the differences between them.
The aim of the project is to make it more accessible for a novice in C++

# Setting up on Windows
## install winget
It might be already installed on Your windows.
If not, or if it doesn't work, try getting it from the windows store. Search for App Installer.

## install MSYS2
`winget install msys2.msys2``

## via MSYS2, install the compilers zoo
``` sh
# !!!!!!! in msys2 terminal !!!!!!!
pacman -S mingw-w64-ucrt-x86_64-gcc
pacman -S gcc gdb
```

## add your msys installation bin dir to your PATH
By default, it will be `C:\msys64\usr\bin`

## build
The command for building that worked for me is 
```
g++ -mwindows -lgdi32 -luser32 -g ${in_file} -o ${out_file}
```
The flags `-mwindows`, `-lgdi32` and `-luser32` allow the compiler to rely on the windows environmental libs. 
The flag `-g` means the debug info will be put into the artifact.

## buid with vscode
The dir already contains config for vscode to build the code via a task.
Run a task: press Ctrl+Shift+P and then select "Run Task", and then select `bulid all CPPs int PROGRAM.EXE`.
