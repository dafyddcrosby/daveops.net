# OpenBSD - CARP
@OpenBSD

master advertises on port 112

## ifconfig syntax

 ifconfig carpN create
 ifconfig carpN [advbase n] [advskew n] [balancing mode]   \
 [carpnodes vhid:advskew,vhid:advskew,...] [carpdev iface] \
 [[-]carppeer peer_address] [pass passphrase] [state state] [vhid host-id]

## Try to become master

 sysctl net.inet.carp.preempt=1

