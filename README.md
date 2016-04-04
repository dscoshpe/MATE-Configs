# MATE-Configs
Configuration files for Wireshark's MATE plugin.

## TCP Conns

`tcp_conns.mate` is a quick and dirty way to mark "complete TCP connections" when they occur.

"Complete TCP connections" refers to TCP sessions that include a packet with only SYN set, and either a packet with either RESET or FIN+ACK set. There is plenty of opportunity to make it smarter by doing full handshake detection for SYN and FIN, but for my purposes it has not been needed.

I use this config for cleaning packet captures for analysis by discarding TCP packets that are not part of a TCP connection. It helps with removing cut off beginnings, endings, and sessions longer than the capture duration.
