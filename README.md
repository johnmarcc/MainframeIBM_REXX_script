# MainframeIBM_REXX_script
REXX script to create a file, write a string in this file and launch a JCL to display the file in a SYSOUT

## Platform 
This REXX script has been written in Visual Studio Code in ZOWE extension

Command to launch the REXXscript:
zowe tso issue command "exec 'z11475.source(rexxjcl)'"   

The string written in the file his:  ""A TEST TO WRITE TO FILE BY JEANM"

wherethe jcl executed in the REXX script is:

//CBL0007J JOB 1,NOTIFY=&SYSUID
//*
//* this jcl is launched by a REXX script
//*
//HEADER EXEC PGM=IEBGENER
//SYSPRINT DD DUMMY
//SYSIN    DD DUMMY
//SYSUT1   DD DSN=Z11475.MYJOHNM,DISP=SHR  
//SYSUT2   DD SYSOUT=*  


## Author
https://github.com/johnmarcc


