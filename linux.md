Text file col to row: 

awk '{for(i=1;i<=NF;i++) printf "%s\n",$i}' input

https://webhostinggeeks.com/howto/how-to-disable-selinux-on-rhel-7centos-7/

find files: 

grep -rnw '/path/to/somewhere/' -e 'pattern'

Linux Disk Space 
 - df –h
 - df
 - sudo du -h / | grep [0-9]G
