# Virtual Box and Virtualization

## What is virtualization?

Virtualization is a process that enables more efficient use of physical computer hardware and is the basis of cloud computing.
Through the use of software, virtualization can divide the hardware components of a single computer, such as its processors,
memory, storage, and other components, into several virtual computers, also known as virtual machines (VMs).
Despite only using a small percentage of the actual underlying computer hardware, each virtual machine runs its own operating system
and functions like a separate computer.

## Virtual Box

![Alt text](https://wjn.sa/wp-content/uploads/2020/10/Breaking-Encrypted-Virtual-Machines-Recovering-VMWare-Parallels-and-VirtualBox-Passwords.jpg "Title")

When using a traditional you need to install the operating system on a physical machine for evaluating software that cannot be installed on your current operating system.
Oracle VirtualBox is what you need in this case, instead of reinstalling software on your physical machine. VirtualBox is designed to run virtual machines on your 
physical machine without reinstalling your OS that is running on a physical machine. One more VirtualBox advantage is that this product can be installed for free.

## Pros of Virtual Box:
### Multiple OS in same computer:
You can run different operating systems on the same computer using virtual box. You are free to configure the system with however much hardware you
want to use. The OS in the virtual box won't occupy a permanent place on the hard disc, just like the genuine OS.

### No effect to host machine: 
On the virtual box, you can also create a virtual hard drive as you establish a virtual machine. The benefit is that the host machine won't even be
affected if the virtual box crashes.
### Latest hardware support:
Both the most recent virtual hardware and outdated hardware are supported. The host computer's USB ports are simple to use and are
compatible with all current USB versions.

## Cons of Virtual Box:
### Less efficient:
Less effective than real machines are the virtual machines on the virtual box. There are some requests that must be granted by the host processor because it is running on the host system.
Usability will suffer as a result.
### Dependent on host machine:
The virtual box can be set up to run the virtual machine at a similar or higher performance level than the host computer.
The virtual machine's direct dependence on the host is due to the fact that it uses the host's hardware.
The virtual machine will be more effective and powerful the faster and more powerful the host.


## Conclusion:
An extensive list of supported operating systems can be utilised with VirtualBox to run a variety of different operating systems.
VirtualBox can be installed on Mac, Windows, Linux, Solaris, and FreeBSD systems. The blog article today described how to install VirtualBox and 
how to utilise it on Windows 10 using the installation of Windows Server 2019 as a guest OS as an example. VirtualBox is open-source, has a user
interface that is uniform across all supported host operating systems, and is free. Instead of installing numerous operating systems on a physical machine 
and rebooting to switch between them, use VirtualBox to run software created for many operating systems on your single physical machine simultaneously.

