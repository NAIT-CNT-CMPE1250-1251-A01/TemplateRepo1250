# Section A02 - Winter 2025 Template

This repository has been set up with an appropriate folder structure for your CMPE1250 class work.

- In-Class Assignments go in the \ICAs folder
- Lab assignments go in the \LABs folder
- Your libraries should only exist in your \Lib folder
- Demo code will be put in the \InClassDemos folder by your instructor
- Some data sheets have been provided in the \Datasheets directory; feel free to add to it
- Exams will be added as submodules throughout the semester

## Libraries

You should not be copying your libraries into individual projects. All of your projects should be using the common library files in the the \Lib folder; there should only ever be one copy of each library file.

## Demo Code

Demo code will be provided to you through out the semester, but it has been included as a sub module; it is a repository inside of a repository.

At the beginning of each day run the following command from the root of your repo:

```github
./update.cmd
```

This is a windows command line script that includes the following, to update the submodule:

```github
git pull
git submodule update --init --remote
git add .
git commit -m "submodule update"
git push
```

## C File Templates

The main directory of this repository contains ```Library Template.c``` and ```Main Template.c```. These should be used as the starting points for your main.c project files and your various library c files. They contain a title block that must be updated and some starter code that should be helpful.

## A note on submitted assignments

Do not modify your ICAs or labs after they have been submitted. If you are going to use them to experiment or practice for an exam, create a new branch or a new directory. This is your repository, you can modify it and add to it as you need to. However, the contents of the assignment folders on the main branch must be ready for instructors to review at all times.

## A note on VS Code Setup

For intellisense and autocomplete to work correctly with the micro controller derivative files, you must tell VS Code where to find the files. With VS Code open, press F1 and type in the following command

```C/C++:EditConfigurations (UI)```

When the configuration page opens, the following directories will need to be added to the C/C++ Include Paths

```windows
${workspaceFolder}/**
${workspaceFolder}/**/Lib 
C:\Program Files (x86)\Freescale\CWS12v5.1\lib/** 
C:\Program Files (x86)\Freescale\CWS12v5.1\lib\hc12c\include/** 

```
