## Room Objectives:

To start with, we will tackle the following topics to build a stepping stone on how to deal with Endpoint Security Monitoring.

- Endpoint Security Fundamentals
- Endpoint Logging and Monitoring
- Endpoint Log Analysis

### Task 1: 
Read the provided instructions and mark the provided question as complete

### Task 2: 
  
### Core Windows Processes

﻿Before we deal with learning how to deep-dive into endpoint logs, we need first to learn the fundamentals of how the Windows Operating System works. Without prior knowledge, differentiating an outlier from a haystack of events could be problematic. 

To learn more about Core Windows Processes, a built-in Windows tool named Task Manager may aid us in understanding the underlying processes inside a Windows machine. 

Task Manager is a built-in GUI-based Windows utility that allows users to see what is running on the Windows system. It also provides information on resource usage, such as how much each process utilizes CPU and memory. When a program is not responding, the Task Manager is used to terminate the process.

A Task Manager provides some of the Core Windows Processes running in the background. Below is a summary of running processes that are considered normal behaviour.

Note: ">" symbol represents a parent-child relationship. System (Parent) > smss.exe (Child)

- System
- System > smss.exe
- csrss.exe
- wininit.exe
- wininit.exe > services.exe
- wininit.exe > services.exe > svchost.exe
- lsass.exe
- winlogon.exe
- explorer.exe
- In addition, the processes with no depiction of a parent-child relationship should not have a Parent Process under normal circumstances, except for the System process, which should only have System Idle Process (0) as its parent process.

### Sysinternals

With the prior knowledge of Core Windows Processes, we can now proceed to discuss the available toolset for analyzing running artefacts in the backend of a Windows machine.

The Sysinternals tools are a compilation of over 70+ Windows-based tools. Each of the tools falls into one of the following categories:

File and Disk Utilities
Networking Utilities
Process Utilities
Security Utilities
System Information
Miscellaneous
We will introduce two of the most used Sysinternals tools for endpoint investigation for this task.

### TCPView - Networking Utility tool.
Process Explorer - Process Utility tool.
TCPView

"TCPView is a Windows program that will show you detailed listings of all TCP and UDP endpoints on your system, including the local and remote addresses and state of TCP connections. On Windows Server 2008, Vista, and XP, TCPView also reports the name of the process that owns the endpoint. TCPView provides a more informative and conveniently presented subset of the Netstat program that ships with Windows. The TCPView download includes Tcpvcon, a command-line version with the same functionality." (official definition)

### Process Explorer

"The Process Explorer display consists of two sub-windows. The top window always shows a list of the currently active processes, including the names of their owning accounts, whereas the information displayed in the bottom window depends on the mode that Process Explorer is in: if it is in handle mode, you'll see the handles that the process selected in the top window has opened; if Process Explorer is in DLL mode you'll see the DLLs and memory-mapped files that the process has loaded." (official definition)

- `Question 1: What is the normal parent process of services.exe?`
`Answer is listed in the provided reading material` -- Hint: Check the note tab
- ` Question 2: What is the name of the network utility tool introduced in this task?`
`Answer is also provided in the reading material as TCPView`
