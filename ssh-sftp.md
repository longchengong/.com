[Home Page](https://longchengong.github.io)
---

# SSH

* Access  
  `ssh remote_username@host_ip`

# SFTP

* Access
`sftp remote_username@host_ip`

* Upload file
`put local_path/filename remote_path/`

* Upload directory
`put -r local_path/ remote_path/`

* Download file
`get remote_path/filename localpath/`

* Commandline
  * Operation in remote host, same with the original commandline
  * Operation in local machine, add prefix "l"
    * `pwd` -> `lpwd`
    * `cd` -> `lcd`
    * `ls` -> `lls`

---
[Home Page](https://longchengong.github.io)
