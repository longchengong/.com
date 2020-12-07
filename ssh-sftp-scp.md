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


---
[Home Page](https://longchengong.github.io)
