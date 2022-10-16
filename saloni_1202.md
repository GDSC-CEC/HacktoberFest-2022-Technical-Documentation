# Virtual Box and Virtualization
If we go through the basic definition, Virtualization relies on software to simulate hardware functionality and create a virtual computer system. This enables IT organizations to run more than one virtual system – and multiple operating systems and applications – on a single server. 
The particular kind of virtualization that allows an unmodified operating system with all of its installed software to run in a special environment, on top of your existing operating system. This environment, called a **"virtual machine"**, is created by the virtualization software by intercepting access to certain hardware components and certain features. 

![Virtual box](https://techgenix.com/tgwordpress/wp-content/uploads/2022/03/1-1.png)

### There are several scenarios that make virtualization attractive:
1. **Operating system** support. With a virtualize such as VirtualBox, one can run software written for one operating system on another (say, Windows software on Linux) without having to reboot.
2. **Infrastructure consolidation**. Since the full performance of today's computers is rarely needed full-time, instead of running many such physical computers, one can "pack" many virtual machines onto a few powerful hosts and balance the loads between them. This can save a lot of hardware costs: e.g., by consolidating many servers into a few. VirtualBox is unique on the virtualization market in that it also allows for consolidating clients onto just a few RDP servers, with full client USB support, while "thin clients" only need to display RDP data.
3. **Testing and disaster recovery**. Especially with the use of snapshots? one can mess with a computing environment by running it as a virtual machine. If something goes wrong, one can easily switch back to a previous snapshot and avoid the need of frequent backups and restores.
## FEATURES
1. Snapshots of the RAM and storage that allow reverting to a prior state.
2. Screenshots and Screen video capture 
3. Special drivers and utilities to facilitate switching between systems
4. Ability to specify amount of shared RAM, video memory, and CPU execution cap
5. Ability to emulate multiple screens
6. Public API  (Java, Python, SOAP, XPCOM)to control VM configuration and execution
7. 2D video output acceleration (not to be mistaken with video decoding acceleration), since version 3.1
8. Mouse pointer integration, meaning automatic coupling and uncoupling of mouse cursor when moved inside and outside the virtual screen, if supported by guest operating system.
9. Seamless mode – the ability to run virtualized applications side by side with normal desktop applications
10. Shared clipboard

## LIMITATION
1. 3D graphics acceleration for Windows guests earlier than Windows 7 was removed in version 6.1. This affected Windows XP and Windows Vista.
2. VirtualBox has a very low transfer rate to and from USB2 devices. 
3. Despite being an open-source product, some of its features are available only in a binary form under a commercial license (see "VirtualBox Extension Pack" below).
4. No cumulative measurement of disk reading and writing like in Microsoft virtual PC. 
5. USB3 devices pass through is not supported by older guest OSes like Vista and Windows XP due to the lack of drivers however starting with version 5.0 VirtualBox offers experimental Renesas uPD720201 xHCL USB3 controller which allows to use USB3 in these operating systems through manual modification of configuration files. 
6. Guest Additions for macOS are unavailable at this time. 
7. Guest Additions for Windows 9x (Windows 95,98 and ME) are not available. This results in poor performance due to the lack of graphics acceleration with the default limited color depth (external third-party software is available to enable support for 32-bit color mode, resulting in better performance). 
8. EFI support is incomplete, e.g., EFI boot for a Windows 7 guest is not supported.
## Conclusion
Virtualization should never be seen as a simple solution to a specific problem; that is the main idea we have been trying to convey. It is a principle, a technology that is applicable in a very large range of different solutions. It is also a buzzword to get cash flowing nowadays, and is heralded by a lot of companies as "the next best thing in IT".
