
- https://www.redhat.com/sysadmin/sort-command-linux

- https://www.redhat.com/sysadmin/uniq-command-lists


Text file col to row: 

awk '{for(i=1;i<=NF;i++) printf "%s\n",$i}' input

Text file field select :

cat u_ex240523.log | awk '{printf "%s\t %s\t %s\n",$1, $2, $22}'

print rest of the fields:

awk '{printf $1;  for(i=3;i<=NF;i++){printf " %s", $i} printf "\n"}' < file

https://webhostinggeeks.com/howto/how-to-disable-selinux-on-rhel-7centos-7/

find files: 

grep -rnw '/path/to/somewhere/' -e 'pattern'

Linux Disk Space 
 - df –h
 - df
 - sudo du -h / | grep [0-9]G

Ref:

 - https://en.wikipedia.org/wiki/Cron
 - https://www.redhat.com/sysadmin/linux-delete-file-rm
 - https://www.redhat.com/sysadmin/recover-file-deletion-linux
