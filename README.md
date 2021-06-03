
### Stephen Yurkin
### 20hrs

## Overview

* This software simulates RAM and loads an executable with a GUI. If the executable is in ‘ELF’ format, the loader will load the executable into ram and calculate the checksum of the entire ram, display the memory in hexadecimal/Ascii, and display the disassmbly for the file. 

## Prerequisites

* Platform: Windows 10
* Software: Visual Studios 2017, ARMSIM # Simulator, NUnit Framework package in Visual Studios

## Build and Test

* With Visual Studios, compiling the project is very simple. To build the solution in Visual Studios under Build, click “Build Solution” (Ctrl + Shirt + B). To run the solution, one can either specify the argument requirements in Visual Studio or open a Command Prompt in the folder where the project executable exists (Usually in bin/Debug). 

* Run the unit test in Visual Studios, go to Test -> Run -> All Tests (Ctrl + R, A). This will run all the unit tests. To run unit tests in Command Prompt, open a Command Prompt and navigate to the folder where the executable. In the Command Prompt, ‘armsim -t’ will run all the unit tests.

## Configurations

* At this stage in the project, there are no configurations.

## User Guide

* armsim [ --l|load elf-file ] [ --m|mem memory-size ] [ --t|test ] [--h|help]

* Usage: loads an ELF file into a simulated RAM (byte array) and
            computes a checksum to verify that the data was loaded correctly.

            Options:
            -l, --load=VALUE           Loads the provided file
            -m, --mem=VALUE            Simulates RAM with provided amount of space.  (Default: 32768 Max: 1MB)
            -t, --test                 Run all unit tests
            -h, --help                 Display help message

* The following can be done with the exe that was loaded in:
    * Step through the ram word-by-word by clicking 'step' or F10. 
    * Run through the ram entirely (With non-responsive GUI)
    * Reload another exe

## Bug Report

* This project doesn’t have the following methods in the Ram class implemented: Run isn't running on a different thread. Therefore the GUI is not active. 

## Project Journal

* https://drive.google.com/file/d/1iIEIsqrInT2OkED9Rs5dGxJho1o01Scz/view?usp=sharing



