# FileProtectorExample
 A C# File Protector Example was implemented with the File Control Filter Driver SDK. The File Control Filter Driver SDK is a kernel-mode component that runs as part of the Windows executive above the file system. The File Control Filter Driver SDK can intercept requests targeted at a file system or another file system filter driver. By intercepting the request before it reaches its intended target, the filter driver can extend or replace functionality provided by the original target of the request. The File Control Filter Driver SDK can log, observe, modify, or even prevent the I/O operations for one or more file systems or file system volumes.
 
![File protector](https://www.easefilter.com/Images/ControlFilter.png)

The File Protector Example can prevent your files from being accessed by unauthorized user. With the File Protector Example  you can control the file I/O activities on file system level, capture file open, create, overwrite, read, write, query file information, set file information, query security information, set security information, file rename, file delete, directory browsing and file close I/O requests.

This C# example creates a filter rule to protect the directory specified at run time. The filter rule was set to protect the folder against the file being renamed, deleted, written. The component is registered with the create and delete IO callback event in the directory. If a file was opened or deleted, the event will be triggered, you can allow or block the IO in the event.


[Read more about file protector example](https://www.easefilter.com/Forums_Files/FileProtector.htm)
