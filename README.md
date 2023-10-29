# VR-spatial-cognition-learning
For the  event-driven GUI dialog the compiling and linking processes, using the MDL development utilities, are supported by the following two batch files.

 Set.bat
 
 set MDL_COMP=-id:\the directory path (local hard disk)

 set RSC_COMP=-id:\the directory path (local hard disk)
 
 set MS=The directory path (local hard disk)
 
 set ACE_DEV=The directory path (local hard disk)


 Build.bat
 
 MicroStation Resource Compiler (creates DCDdlg.rsc)
 rcomp DCDdlg.r

 MDL Compiler (creates DCD.mo)
 mcomp -v -c DCD.mc

 MDL Linker (creates DCD.mp)
 mlink -aDCD.mp DCD.mo

 Resource Librarian (creates the final executable file DCD.ma)
 rlib -oDCD.ma DCD.mp DCDdlg.rsc

 copy DCD.ma The-directory-path (local hard disk)
