# mesh-network
golang learning project

# implementation
vague idea of a tailscale-like mesh network that should be easy to self host and not need central proxy server with its own public IP address

- on connect, client should use STUN 5389 to get public ip and port 
- connect to a replicated database hosted on a cloud service and store public IP and port
- get peer public IP and port from database, and setup peer endpoint

works the exact way as stunmesh-go, but hopefully with a simpler implementation
- only need to support Linux, so can embed wireguard-go module

# notes
- https://github.com/tjjh89017/stunmesh-go
- https://speakerdeck.com/tjjh89017/fosdem-2026-stunmesh-go-building-p2p-wireguard-mesh-without-self-hosted-infrastructure
