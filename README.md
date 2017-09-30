# What's this

This is Richard Stevens' sock program metioned in _TCP/IP Illustrated_ Vol.1, and updated by Christian Kreibich so that it can run on Linux FreeBSD and Mac OS X, I just transported it to github.

You can visit the program in [http://www.icir.org/christian/sock.html](http://www.icir.org/christian/sock.html), or visit the author's mainpage in [http://www.icir.org/christian/index.html](http://www.icir.org/christian/index.html)

# How to install
```
bash autogen.sh
./configure
make
sudo make install
```

#How to use 
```
usage: sock [ options  ] <host> <port>       (for client; default)
sock [ options  ] -s [ <IPaddr>  ] <port>     (for server)
sock [ options  ] -i <host> <port>           (for "source" client)
sock [ options  ] -i -s [ <IPaddr>  ] <port>  (for "sink" server)
options: -b n  bind n as client's local port number
  -c    convert newline to CR/LF & vice versa
  -f a.b.c.d.p  foreign IP address = a.b.c.d, foreign port# = p
  -g a.b.c.d  loose source route
  -h    issue TCP half close on standard input EOF
  -i    "source" data to socket, "sink" data from socket (w/-s)
  -j a.b.c.d  join multicast group
  -k    write or writev in chunks
  -l a.b.c.d.p  client's local IP address = a.b.c.d, local port# = p
  -n n  #buffers to write for "source" client (default 1024)
  -o    do NOT connect UDP client
  -p n  #ms to pause before each read or write (source/sink)
  -q n  size of listen queue for TCP server (default 5)
  -r n  #bytes per read() for "sink" server (default 1024)
  -s    operate as server instead of client
  -t n  set multicast ttl
  -u    use UDP instead of TCP
  -v    verbose
  -w n  #bytes per write() for "source" client (default 1024)
  -x n  #ms for SO_RCVTIMEO (receive timeout)
  -y n  #ms for SO_SNDTIMEO (send timeout)
  -A    SO_REUSEADDR option
  -B    SO_BROADCAST option
  -C    set terminal to cbreak mode
  -D    SO_DEBUG option
  -E    IP_RECVDSTADDR option
  -F    fork after connection accepted (TCP concurrent server)
  -G a.b.c.d  strict source route
  -H n  IP_TOS option (16=min del, 8=max thru, 4=max rel, 2=min$)
  -I    SIGIO signal
  -J n  IP_TTL option
  -K    SO_KEEPALIVE option
  -L n  SO_LINGER option, n = linger time
  -N    TCP_NODELAY option
  -O n  #ms to pause after listen, but before first accept
  -P n  #ms to pause before first read or write (source/sink)
  -Q n  #ms to pause after receiving FIN, but before close
  -R n  SO_RCVBUF option
  -S n  SO_SNDBUF option
  -T    SO_REUSEPORT option
  -U n  enter urgent mode before write number n (source only)
  -V    use writev() instead of write(); enables -k too
  -W    ignore write errors for sink client
  -X n  TCP_MAXSEG option (set MSS)
  -Y    SO_DONTROUTE option
  -Z    MSG_PEEK
```

(cc) Christian Kreibich 
