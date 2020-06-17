# nogfw

# install
``` bash
apt install libpcap-dev libnetfilter-queue-dev -y
git clone https://github.com/4D4937/nogfw.git
iptables -A OUTPUT -p tcp --tcp-flags SYN,ACK SYN,ACK --sport 1:65535 -j NFQUEUE --queue-num 0
cd nogfw
./f_gfw
```
