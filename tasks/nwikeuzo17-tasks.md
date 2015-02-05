Here are some simple tasks:
i)  To rename a file, we can use the mv command, which can also serve to move a file. To rename a file,   
    the syntax would be mv filename newfilename, where filename is the current file name and newfilename is the new name. 
    To move a file into a new directory, the syntax would be mv filename newdirectory, where newdirectory is the directory 
    the file is to be moved to.
ii) Determine the size of a file: ls --block-size=M gives the size of a file in MB. For files less than 1MB in size, it returns 1MB. ls –lh gives the size in gigabytes if the file is up to a gigabyte.
iii) Display the first ten lines of a file: head big
     Display the first twenty five lines of a file: head -25 big
     Display the last ten lines of a file: tail big
     Display the last twenty five lines of a file: tail -25 big
