# cshell
Minimal Unix Cell developed in C Programming Language

>⚠ Note: This is a programming project of the System Programming class (CPE 357) at Cal Poly. According to the Collaboration Agreement of the Institution regarding Code Distribution, I cannot make my source code of this project public. Please feel free to reach out to me if you need further access to this project.

## Features
* Support Unix commands
* Support up to 1024 characters per line
* Support File Redirection 
* Support a pipeline of up to 20 commands
* Exit the Shell by either using the “exit” command or triggering EOF
 
 ***
# Project Overview
Please take a few minutes to review the overview below:

## Development Process
The development process took me about two weeks to finish. The process went through three stages: developing the Pipeline system for the C Shell, implementing the C Shell program, and testing the program.

When developing the Pipeline system for the C Shell, I did not excessively make a System call pipe() and create an excessive number of file descriptors (FDs). Instead, I carefully managed the Pipeline system by opening and closing the FDs at appropriate places in both the parent and the child processes. By doing that, I only used at most five FDs to set up my pipeline system for an indefinite number of child processes. 

When implementing the C Shell Program, a significant problem I solved regarding the File Redirection feature.  By default, several Linux processes get input from stdin and print output to stdout. To redirect the default I/O behaviors of these processes, I learned and used the "dup2" function in C.

After these two stages, I developed an effective test suite for the project and learned writing bash scripts to run all tests with a single command.
