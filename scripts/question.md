A text editor is used to create an executable script. One of the text editor tools, vi, or the improved vi version, vim, is based on letter and number-based commands to modify text. For example, dd will delete the whole line on which the cursor is placed. 5dd would delete 5 lines. When vi is in command mode, input is interpreted as a command.

To enter insert mode at the current cursor position type **i**. To append text at the end of the current line, type **a**. To insert text on a new line below the current line, type **o**. Use the Esc key to exit out of insert mode to command mode.

To save a file in the vi editor use **:w** from command mode. To save and quit, type **:wq**. To quit without saving type **:q!**.

Depending on your version of Unix-like OS, you may find other text editor tool, such as nano, pico, and gedit. The text editing tools, such as vi, nano, and pico, are accessible through the command line; while the GUI-based text editors, like gedit, may be located via the application menu or the command line.

1.    Start up a Linux computer or VM.
2.    Use a text editor tool and create a file named **info.sh** in your home directory with the following text:

```  
  #!/bin/bash
  echo “Computer name is: “  $HOSTNAME
  echo “Operating System is:”
  cat /etc/os-release | grep PRETTY_NAME
  echo “CPU is”
  lscpu | grep “Model name:” | sed -r ‘s/Model name:\s{1,}//g’
  echo “Total Memory is”  
  cat /proc/meminfo | grep  “MemTotal“
  echo “The disks that are installed and their freespace“
  df -h
  echo “All the” $HOSTNAME “IP addresses”
  hostname -I
```

3.    Open a terminal and navigate to your home directory. To make the script executable, enter chmod 755 info.sh at prompt.
4.    At the prompt, enter ./info.sh to execute the script.

Questions:

# What is the output of the script?


