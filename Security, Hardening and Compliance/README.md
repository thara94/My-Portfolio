# Downloading and installing Lynis step by step and a script to monitor the health of a server.

Ubuntu

1. After starting the Ubuntu server install Lynis by running the “Sudo git clone https://github.com/CISOfy/lynis”
2. After installation is done run the Lynis by running the following commands “cd lynis” to get to the lynis directory. Then “./lynis audit system” to run lynis
3. Lynis report can be found under lynis-report.dat
4. Then install dstat by running “sudo apt-get install sysstat” to use mpstat in the script 
5. Then install atop by typing “sudo install atop”
6. Then create Sscript for different command that can be use in mentoring the server. 
7. Vi sscript.
8. Click insert key, then type the script.
9.The first command is “sudo free”: this command to checks the server memory usage.
10. The second command is “sudo mpstat”: this command to take snapshot of CPU usage.
11.The third command is “sudo lsof”: to look at all the open files.
12. Then an if statement to ask the user if wants to run atop command, if the answer is yes then “sudo atop” command would run to provide information about the system performance.
13. At the end the scrip ask user if wants to save the output into a file if answer is yes the running command output will be added to a file called info
14.  Click ESC key and then :wq to exit the vim.
15.  Make the script executable by running chmod +x script-name and path, and then run the script by typing ./script-name
 
 
 

