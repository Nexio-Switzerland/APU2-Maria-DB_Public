# Webmin

## Mounting an CIFS filesystem
smbfs (samba file system) or cifs (common internet file system) is the protocol used by Windows systems to share files with each other. If you have files on a Windows system that you want to access on your Linux system, you must first share the directory and assign it a share name using the Windows user interface.

Once that is done, follow these steps to mount the share on your Unix system :

1. On the main page of the Disk and Network Filesystems module, select Common Internet File System from the drop-down box of filesystem types, and click the Add mount button. A form will appear as shown below.
2. In the Mounted As field, enter the directory on which you want the filesystem to be mounted. The directory should be either non-existent or empty, as any files that it currently contains will be hidden once the filesystem is mounted.
3. If you want the filesystem to be mounted at boot time, select Save and mount at boot for the Save Mount option. If you want it to be permanently recorded but not mounted at boot, select Save. Otherwise, select Don't save if this is to be only a temporary mount.
4. For the Mount now? option, select Mount if you want the filesystem to be mounted immediately, or Don't mount if you just want it to be recorded for future mounting at boot time.
5. In the Server Name field, enter the hostname or IP address of the Windows server. The button next to the field will pop up a list of Windows servers on your network, requested from the domain or workgroup master set in the module configuration.
6. In the Share Name field, enter the name of the share. This will be something like movies, not the full path on the Windows server like c:\files\movies. If you have entered the server name, clicking on the button next to the field will pop up a list of available shares.
7. If the Windows server requires a username and password to access the file share, fill in the Login Name and Login Password fields. If no authentication is needed, these fields can be left blank.
8. Because Windows networking has no concept of Unix users, when the filesystem is mounted all files from the fileserver will be owned by a single Unix user and group. By default that user is root, but you can change this by filling in the *User files are owned by* and Group files are owned by fields.
9. Click the Create button at the bottom of the page to mount and/or record the filesystem. If all goes well, you will be returned to the filesystems list. Otherwise, an error will be displayed explaining what went wrong.
![image](https://user-images.githubusercontent.com/97556752/221190382-aa9ecbbd-ea6f-4b32-bd58-f9c4fb141a95.png)
