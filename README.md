CreateSwap
==========
CreateSwap is a Python script that manages Linux swap files. 
You can create and delete swap files very quickly without using makeswap, swapon, ... commands.
Just specify the file and its size and let everything is done by CreateSwap.

Usage
==========
Since managing swap files requires root access, CreateSwap must be executed using sudo command or
if not, root password is asked automatically.

Executing the script without specifying any option prints help.

To create a swap file, two options must be specified:

 * **-f** which sets the files
 * **-s** which sets the size in megabytes
  
To delete an already created swap file **-o** option - which stands for off - following by the file
name is necessary.

The **--verbose** option runs the script in the verbose mode which is useful when an error occurred.

NOTE: "python.py" WORKS ONLY WITH PYTHON VERSION 3. FOR PYTHON 2, USE "createswap2.py".

Examples
==========

```
$ python ./createswap.py -f swapfile -s 512
$ python ./createswap.py -f /var/swapfile -s 2048 --verbose
$ python ./createswap.py -o /var/swapfile --verbose
```


This script can be executed directly if its file has the executable permission.

```
$ ./createswap.py -f swapfile -s 512
$ ./createswap.py -f /var/swapfile -s 2048 --verbose
$ ./createswap.py -o /var/swapfile --verbose
```

Further Reading
==========
To read more please visit our [CodeProject page](http://www.codeproject.com/Tips/785674/Creating-Linux-Swap-Files-Using-Python).
