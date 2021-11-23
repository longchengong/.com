[Home Page](https://longchengong.github.io)
---

# SSH

* Access
  `ssh remote_username@host_ip`

* Local port forward  
  `ssh remote_username@host_ip -L local_port1:remote_host1:remote_port1 -L local_port2:remote_host2:remote_port2 -L ...`

* Remote port forward  
  `ssh remote_username@host_ip -R remote_port1:dest_host1:dest_port1 -R remote_port2:dest_host2:dest_port2 -R ...`  

  `ssh remote_username@host_ip -R remote_port1:127.0.0.1:destination_port1`

# SFTP

* Access
  `sftp remote_username@host_ip`

* Upload file
  `put local_path/filename remote_path/`

* Upload directory
  `put -r local_path/ remote_path/`

* Download file
  `get remote_path/filename local_path/`

* Commandline
  + Operation in remote host, same with the original commandline
  + Operation in local machine, add prefix "l"
    - `pwd` -> `lpwd`
    - `cd` -> `lcd`
    - `ls` -> `lls`

# SCP

* Copy local file to remote host
  `scp local_path/filename remote_username@host_ip:/remote_path/`

* Copy local diretory to remote host
  `scp -r local_path remote_username@host_ip:/remote_path/`

* Copy remote file to local
  `scp remote_username@host_ip:remote_path/filename local_path/`

* Copy remote directory to local
  `scp -r remote_username@host_ip:remote_path local_path/`

# Device/OS Info
* General OS Info
  `top`
* CPU/Mememory/Linux kernel Info
  + `cat /proc/cpuinfo`
  + `cat /proc/meminfo`
  + `cat /proc/version`
* List Hard Disk Partion
  + `fdisk -l`
* list block devices (combine with fdisk -l)
  + `lsblk` 
* report file system disk space usage
  + `df -H/h` -- dish free
* OS name & version for Redhat
  + In Debian: `/etc/debian_version`
  + In Ubuntu: `lsb_release -a or /etc/debian_version`
  + In Redhat: `cat /etc/redhat-release`
  + In Fedora: `cat /etc/fedora-release`

# Zip/Unzip
 + Zip: `zip -r tgt.zip a b c/` 
 + Unzip: `unzip src.zip`  

# Tape archive(tar)
  + Create: `tar -cvf tgt.tar a b c/`
  + Extract: `tar -xvf src.tar`  

# Check Login Activities
  + Show who is logged on and what they are doing: `w`
  + Show who is logged on: `who`
  + Show last logged on: `last`
  + Show bad login attempt: `lastb`

# Network connections/Socket
  + Show info related to listening port: `lsof -i :port`
  + Show sockets info with state and source/destination host and src/dst port:  
      `ss -anp state listening/established src/dst ip sport/dport [= \> \<] :port`
  + Show info related to port(Linux/Windows): `netstat -anp | grep port` `netstat -ano | findstr port`


---
[Home Page](https://longchengong.github.io)
