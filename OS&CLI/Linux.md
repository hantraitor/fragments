[File System Permission - Regular File]  
Two methods to execute a script, whose permission requirements are:  
Directly executing the script, requires read+execute  
Having the interpreter call the script, only requires read  

One method to execute a binary file, whose permission requirements are:  
Directly executing the file, only requires execute  

[File System Permission - Directory]  
Read alone: can only see the name and type of its childs, by listing the directory  
Write alone: can do nothing  
Execute alone: can cd to the directory; can deal with its childs (according to permissions on childs) if childs are exactly named  
