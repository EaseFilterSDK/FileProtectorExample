# [File Protector Example](https://www.easefilter.com/Forums_Files/FileProtector.htm)
 A C# File Protector Example was implemented with the File Control Filter Driver SDK. The File Control Filter Driver SDK is a kernel-mode component that runs as part of the Windows executive above the file system. The File Control Filter Driver SDK can intercept requests targeted at a file system or another file system filter driver. By intercepting the request before it reaches its intended target, the filter driver can extend or replace functionality provided by the original target of the request. The File Control Filter Driver SDK can log, observe, modify, or even prevent the I/O operations for one or more file systems or file system volumes.
 
![File protector](https://www.easefilter.com/Images/ControlFilter.png)

The File Protector Example can prevent your files from being accessed by unauthorized user. With the File Protector Example  you can control the file I/O activities on file system level, capture file open, create, overwrite, read, write, query file information, set file information, query security information, set security information, file rename, file delete, directory browsing and file close I/O requests.

## File Access Control and File Protection

With the EaseFilter File Access Control SDK you can control the file I/O activities on file system level, capture file open, create, overwrite, read, write, query file information, set file information, query security information, set security information, file rename, file delete, directory browsing and file close I/O requests. 

## Protect Your Files with File Protection Policies 

### Control the file I/O with access flags.

You can set the access flag to control the file access in the file filter rule. With the access flag of the filter rule, you can use every bit of the access flag integer to allow or block the specific I/O as below to run.

-  **ALLOW_ENCRYPT_NEW_FILE**: Allow to encrypt the new created file if the encryption filter rule is enabled.
-  **ALLOW_READ_ENCRYPTED_FILES**: Allow the encrypted files being read, or the raw encrypted data will return.
-  **DISABLE_ENCRYPT_DATA_ON_READ**: Encrypt the file on the go when it is false when encryption filter rule is enabled, it will encrypt unencrypted data on read.
-  **ENABLE_HIDE_FILES_IN_DIRECTORY_BROWSING**: Hide the files from the folder directory list if the hide file mask was added.
-  **ENABLE_REPARSE_FILE_OPEN**: Reparse the file open to the new file name if the reparse file mask was added.
-  **ALLOW_FILE_ACCESS_FROM_NETWORK**: Allow the file being accessed via SMB share.
-  **ALLOW_COPY_PROTECTED_FILES_OUT**: Allow the file being copied out of the protected folder.
-  **ALLOW_COPY_PROTECTED_FILES_TO_USB**: Allow the file being copied out of the USB drive.
-  **ALLOW_OPEN_WTIH_ACCESS_SYSTEM_SECURITY**: Allow the file open to access the file's security information.
-  **ALLOW_OPEN_WITH_READ_ACCESS**: Allow the file open for read access.
-  **ALLOW_OPEN_WITH_WRITE_ACCESS**: Allow the file open for write access.
-  **ALLOW_OPEN_WITH_CREATE_OR_OVERWRITE_ACCESS**: Allow you to create new file or open file with overwrite access.
-  **ALLOW_OPEN_WITH_DELETE_ACCESS**: Allow the file open for delete.
-  **ALLOW_READ_ACCESS**: Allow the file data being read.
-  **ALLOW_WRITE_ACCESS**: Allow the file being written.
-  **ALLOW_QUERY_INFORMATION_ACCESS**: Allow to query file information.
-  **ALLOW_SET_INFORMATION**: Allow to change the file information: change file attribute, change file size, rename file name, delete file.
-  **ALLOW_FILE_RENAME**: Allow the file being renamed.
-  **ALLOW_FILE_DELETE**: Allow the file being deleted.
-  **ALLOW_FILE_SIZE_CHANGE**: Allow the file size being changed.
-  **ALLOW_QUERY_SECURITY_ACCESS**: Allow the file security information being queried.
-  **ALLOW_SET_SECURITY_ACCESS**: Allow the file security information being changed.
-  **ALLOW_DIRECTORY_LIST_ACCESS**: Allow you to browse the directory files.

### Control the file I/O by registering the I/O callback notification event.

You can register the file I/O events to control the file access in the file filter rule. By registering the specific I/O events, you can fully control the I/O, your callback functions will be invoked for every registered I/O, you can allow, modify or block this I/O based on the I/O information.

-  **OnPreFileCreate**: Fires this event before the file create IO was going down to the file system.
-  **OnPostFileCreate**: Fires this event after the file create IO was returned from the file system.
-  **OnPreFileRead**: Fires this event before the file read IO was going down to the file system.
-  **OnPostFileRead**: Fires this event after the file read IO was returned from the file system.
-  **OnPreFileWrite**: Fires this event before the file write IO was going down to the file system.
-  **OnPostFileWrite**: Fires this event after the file write IO was returned from the file system.
-  **OnPreQueryFileSize**: Fires this event before the query file size IO was going down to the file system.
-  **OnPostQueryFileSize**: Fires this event after the query file size IO was returned from the file system.
-  **OnPreQueryFileBasicInfo**: Fires this event before the query file basic info IO was going down to the file system.
-  **OnPostQueryFileBasicInfo**: Fires this event after the query file basic info IO was returned from the file system.
-  **OnPreQueryFileStandardInfo**: Fires this event before the query file standard info IO was going to the file system.
-  **OnPostQueryFileStandardInfo**: Fires this event after the query file standard info IO was returned from the file system.
-  **OnPreQueryFileNetworkInfo**: Fires this event before the query file network info IO was going down to the file system.
-  **OnPostQueryFileNetworkInfo**: Fires this event after the query file network info IO was returned from the file system.
-  **OnPreQueryFileId**: Fires this event before the query file Id IO was going down to the file system.
-  **OnPostQueryFileId**: Fires this event after the query file Id IO was returned from the file system.
-  **OnPreQueryFileInfo**: Fires this event before the query file info IO was going down to the file system
-  **OnPostQueryFileInfo**: Fires this event after the query file info IO was returned from the file system.
-  **OnPreSetFileSize**: Fires this event before the set file size IO was going down to the file system.
-  **OnPostSetFileSize**: Fires this event after the set file size IO was returned from the file system.
-  **OnPreSetFileBasicInfo**: Fires this event before the set file basic info IO was going down to the file system.
-  **OnPostSetFileBasicInfo**: Fires this event after the set file basic info IO was returned from the file system.
-  **OnPreSetFileStandardInfo**: Fires this event before the set file standard info IO was going down to the file system.
-  **OnPostSetFileStandardInfo**: Fires this event after the set file standard info IO was returned from the file system.
-  **OnPreSetFileNetworkInfo**: Fires this event before the set file network info was going down to the file system.
-  **OnPostSetFileNetworkInfo**: Fires this event after the set file network info was returned from the file system.
-  **OnPreMoveOrRenameFile**: Fires this event before the file move or rename IO was going down to the file system.
-  **OnPostMoveOrRenameFile**: Fires this event after the file move or rename IO was returned from the file system.
-  **OnPreDeleteFile**: Fires this event before the file delete IO was going down to the file system.
-  **OnPostDeleteFile**: Fires this event after the file delete IO was returned from the file system.
-  **OnPreSetFileInfo**: Fires this event before the set file info IO was going down to the file system.
-  **OnPostSetFileInfo**: Fires this event after the set file info IO was returned from the file system.
-  **OnPreQueryDirectoryFile**: Fires this event before the query directory file info was going down to the file system.
-  **OnPostQueryDirectoryFile**: Fires this event after the query directory file info was returned from the file system.
-  **OnPreQueryFileSecurity**: Fires this event before the query file security IO was going down to the file system.
-  **OnPostQueryFileSecurity**: Fires this event after the query file security IO was returned from the file system.
-  **OnPreSetFileSecurity**: Fires this event before the set file security IO was going down to the file system.
-  **OnPostSetFileSecurity**: Fires this event after the set file security IO was returned from the file system.
-  **OnPreFileHandleClose**: Fire this event before the file handle close IO was going down to the file system.
-  **OnPostFileHandleClose**: Fires this event after the file handle close IO was returned from the file system.
-  **OnPreFileClose**: Fires this event before the file close IO was going down to the file system.
-  **OnPostFileClose**: Fires this event after the file close IO was returned from the file system.

## How To Develop File Protection Application with a C# example

In this file protector example you can create different filter rules to protect the directory specified at run time. With the filter rules you can protect your folders against the file being renamed, deleted or written, you can modify the file I/O data by registering the file I/O notification event.

[Read more about EaseFilter File Access Control SDK](https://www.easefilter.com/Forums_Files/FileProtector.htm)
