### Redesigned V6 file system
This modified version of V6 file system will support a file size up to 4GB. 

### Compile instructions
To compile the code run the following command 

```
gcc fsaccess.c -o fsaccess -lm
```

### Executing the code 
To execute the complied code run ``` ./fsaccess ***filename***``` this will open a command line interface for user to input various file system commands. 

These are the following commands we have implemented
1. initfs 
2. cpin
3. cpout
4. mkdir
5. Rm
6. q

### initfs command

initfs can take three arguments.
initfs 'filename' 'no.of.blocks assigned to the file'  'no of inodes assigned to the file'

Example code will of this format ``` initfs v6file 8000 200```
Above code will generate the following output
```
cmd initfs
v6file
Init file_system was requested: v6file
Total blocks :8000, Total inodes:200

Initialized a new filesystem with 8000 number of blocks and 200 number of i-nodes, size of one i-node 64

Bytes (8192000) written, block size 1024
Directory in the block 5
File system successfully initialized
```

It prints out the no of bytes written and the directory block in which the file resides.
### cpin command
After the user creates a file system using the initfs ```cpin from_filename to_filename``` will take two arguments from filename and  to filename.

### cpout command
cpout ```cpout from_filename to_filename ```out command takes two command from filename and to filename.
### Rm command
Rm command takes input of the filepath that will be removed from the filesystem if it exists ```Rm filename```.
### mkdir command 
mkdir command takes input of the filepath that will be created in the filesystem if it doesnot exists ```mkdir filename```.
### q command
when user enters q the program exist from the file system. 



