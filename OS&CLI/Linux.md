[File System Permission - Regular File]  
Two methods to execute a script, whose permission requirements are:  
Directly executing the script, requires read+execute  
Having the interpreter call the script, only requires read  

One method to execute a binary file, whose permission requirements are:  
Directly executing the file, only requires execute  

[File System Permission - Directory]  
Read alone: can only see the name and type of its childs (the level directly under the directory), by listing the directory  
Write alone: can do nothing  
Execute alone: can cd to the directory; can deal with its childs (according to permissions on childs) if each child is cited with exact name  
Read+write: = read alone  
Read+execute: = read alone + execute alone  
Write+execute: = execute alone + create/move/delete childs  

[File System Permission - SUID/SGID/Sticky Bits]  
SUID: effective only on binary executables (not on scripts)  
SGID: effective only on binary executables (not on scripts), or on directories  
Sticky: effective only on directories (other Unix and like systems may be different)  

### [Shell - combining multiple commands]
* Commands separated by ; are executed in sequence, regardless of errors
* Commands following && || are executed based on last exit status
* Commands enclosed by () are executed as a group in a child shell, comparable to directly executing a script
* Commands enclosed by {} are executed as a group in the current shell, comparable to "source script"  
  _#NOTICE that a space or line feed must follow { before enclosed commands_  
  _#NOTICE that ; must be appended to the last enclosed command too_  
  _#e.g. { ls;}_
* Other methods may be used for specific situations:
  * Command substitution $() ``
  * Pipe |
