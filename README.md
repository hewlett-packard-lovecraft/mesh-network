# mesh-network
golang learning project

# implementation
a tailscale-like mesh network that should not need a proxy server with its own public IP address

- on connect, client should use STUN 5389 to get public ip and port 
- connect to a replicated database hosted on a cloud service and store public IP and port
- get peer public IP and port from database, and setup peer endpoint

should work the exact way as stunmesh-go (cloudflare DNS TXT records)  & wireguard-p2p (distributed k/v store) but with relational DB instead.
- because we use a relational database instead of a k/v store, we can more easily store local ip/port in addition to public ip/port.
- only need to support Linux, so can embed wireguard-go module


# notes
- https://github.com/tjjh89017/stunmesh-go
- https://speakerdeck.com/tjjh89017/fosdem-2026-stunmesh-go-building-p2p-wireguard-mesh-without-self-hosted-infrastructure
- notes on lan/wan path selection https://nordsecurity.com/blog/reaching-beyond-1gbps
