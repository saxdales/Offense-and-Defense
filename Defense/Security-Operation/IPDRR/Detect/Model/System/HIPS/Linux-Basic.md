## `Summary`
- Design thinking
- Directory
- 

## `Design thinking`
 - _Everything is file_ : 
 
  File can be understood as super class, derive class included common file, device, network socket, process and pipe.The best benefit is you can use API of file to handle all thse, such as read, write and close.

## `Directory`
### /proc directory
  Proc is a vrtual file system, providing a interface pointing to kernel data struct with a format of system file directory. With it we can check and modify system property.
   Generally it contains files and directories as follows:
  
  | directory  | information |
| ------------- | ------------- |
| /proc/pid | info about pid : ls -al /proc |
| /proc/self | another process calling this link will call the pid |
| /proc/pid/attr | provide API for security module : SELinux |
| /proc/pid/cmdline | complete commands of process  |
| /proc/pid/cwd | working directory of current process   |
| /proc/pid/environ | environment variables the process started with execve |
| /proc/pid/exe | signal link of executable file |
| /proc/pid/fd/ | file discriptors the process opened : 0 & 1 & 2 |
| /proc/pid/fdinfo/ |info of fd : offset & visit flags |
| /proc/pid/maps | memory address & permission |
| /proc/net | record information about network |
| /dev/tty | teletype : virtual console  |
| /dev/pty| pseudo : remote login ternimal shell |

## `Command`
### File
 Linux system limites different users to access the same file. We can use ll or ls -l to check the file owner and attribute.
- chown : modify the owner
- chmod : modify the privilege

### Data Process
- grep
- awk -F 
- 

### Reference
- [Master the command line, in one page](https://github.com/jlevy/the-art-of-command-line)


## `Process`
 Process is a running program. Every process is created by fork() syscall.
- process tree
  - command: pstree
  - parent /children /ancestor process

## `Tracing`
- [Linux tracing - kprobe, uprobe and tracepoint](https://terenceli.github.io/%E6%8A%80%E6%9C%AF/2020/08/05/tracing-basic) @terenceli

## `Reference`
- [linux-basics-for-the-aspiring-hacker](https://www.hackers-arise.com/post/2016/08/04/linux-basics-for-the-aspiring-hacker-part-1)
