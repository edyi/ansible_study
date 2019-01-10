### command
``` 
ansible-playbook ****.yml 
```

### その他
テストのためrootでノンパス設定（鍵認証）


master -ssh-> slaveのとき鍵が変わっても警告を出さないようにする
```
Host slave
HostName slave
User root
IdentityFile /root/.ssh/id_rsa
ServerAliveInterval 60
TCPKeepAlive yes
StrictHostKeyChecking no
UserKnownHostsFile=/dev/null
```
