# nogfw

It rewrites the TCP window size announced in this segment. The window size is rewritten to a smaller, randomly chosen value. 
That way, the client "fragments" its cipher list inside the TLS client hello. 

# install

`git clone https://github.com/4D4937/nogfw.git`

`iptables -A OUTPUT -p tcp --tcp-flags SYN,ACK SYN,ACK --sport 1:65535 -j NFQUEUE --queue-num 0`

``` bash
git clone https://github.com/4D4937/nogfw.git
iptables -A OUTPUT -p tcp --tcp-flags SYN,ACK SYN,ACK --sport 1:65535 -j NFQUEUE --queue-num 0
./nogfw
```
