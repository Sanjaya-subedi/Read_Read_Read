William Stallings

Part I - Background

Starts with simple overview before diving into deep concepts. It talks about principal kernel components: signals, system calls, processes and scheduler, virtual memory, file systems, network protocols, character device drivers, block device drivers, network device drivers, traps and faults, physical memory and interrupts.

Talks about Android Operating system, uses linux but this OS is customized in a way suitable for mobile phones and apps. For applications it supports application frameworks like activity manager, window manager, package manager, telephony manager, content providers, resource manager and it supports system libraries like media framework sqlite, android runtime core librearies like openGL/ES, linxu kernel for camera and bluetooth driver, .. view system, location manager, notification manager. System libraries are the layer below application framework and consist of two parts: system libraries and android runtime. 

One realization for me: since html are markup languages and browsers only can execute these, we have browser enginer as a system library in android os that uses webkit library that is used for fast display of html.

Android kernel lacks drivers not applicable in mobile env so kernel is smaller. 

Android runtime, it talks about dalvik VMs, this is language VM, not system VM.

Activities: An activity is a single visual user interface component, including objects such as menu, icon, checkboxes. Also android has two features to enhance the ability to peform power management, alarms and wakelocks. The alarms capability is implemented in the linux kernel, and is visible to the app developer through alarm manager and wakelock facility prevents an android system from entering into sleep mode.

PART -2  Processes
Process is an instance of execution of program. IT has many elements that helps to distinct with other process. Identifier, state, priority, program counter, memory pointers, context data, i,o satus, accounting info. These information are stored in a data structure called process control block. So, a process consists of a program code and associated data plus a process control block. 

Process creation
In a batch env, a process is cerated in response to the submission of a job or in an interactive env, a process is created when a new user attempts to log on. Also, there is chance of one process to cause the creation of another. When the OS creates a process at the explicit request of another process, the action is called process spawning. When one process spawns another, the former is called parent process and the spawned one is child process. 