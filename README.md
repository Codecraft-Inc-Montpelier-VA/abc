This directory can be used to generate the abc executable as well as its 
literate program (abc.pdf).

The layout for this directory is:

abc tree
--------
|-- Makefile
|-- Debug
|    +-- abc.o
|    +-- abc
|-- Release
|    +-- abc.o
|    +-- abc
|-- doc
|    +-- abc.pdf
|-- include
|    +-- sccorlib.h
|-- code
    +-- abc.cpp

Run “make clean” to remove previously built .cpp, .o, executable, and .pdf files.
Run “make doc” to create just the doc/abc.pdf literate program.
Run “make code” to create just the code/abc.cpp source file.
Run “make outfile” to create just the Debug/abc executable file.
Run “make” to create both the abc executable and the abc.pdf literate program.

The above commands build a Debug version of the abc executable.  To build a Release 
version of the abc executable, include the option "CFG=Release" in the make command.
For instance, run “make CFG=Release clean; make CFG=Release outfile” to create a 
Release version of the abc executable file.

Building the abc executable requires the Simple C/C++ Coroutines library (sccorlib.a) 
and its header file (include/sccorlib.h).  The sccorlib.a file is built elsewhere.


