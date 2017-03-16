# hpn-ssh-archive

## About
https://www.psc.edu/hpn-ssh

## Build & Install (ubuntu16.04)
I'll rely on my memory to write.
```
$ sudo apt install -y zlib1g-dev libssl-dev 
$ git clone https://github.com/d0n0/hpn-ssh-archive.git
$ cd ./hpn-ssh-archive
$ tar zxvf openssh-7.2p2.tar.gz
$ cd ./openssh-7.2p2
$ patch ../openssh-7_2_P2-hpn-14.10.diff
$ ./configure --prefix=/usr/local
$ make
$ sudo make install
```

## Managing sshd-service with systemd
```
$ sudo cp sshd.service /etc/systemd/system/
$ sudo systemctl reload-daemon
$ sudo systemctl enable sshd.service
```
