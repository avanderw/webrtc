# WebRTC Tech Demo

This is a tech demo for WebRTC.
The goal is to establish a serverless connection between multiple clients.
Any infrastructure required should be minimal and free. Thus, no TURN server.

## Goals

- [x] One html file per concept.
- [x] Same device, same tab.
- [x] Same device, different tabs.
- [x] Same device, different browsers.
- [ ] Different devices, same network.
- [ ] Different devices, different networks.
- [ ] Establish a stable serverless connection between multiple clients using WebRTC.

## Quickstart

Open the `index.html` file in your browser.

## Motivation

I want maintenance to be minimal so that the lifetime of the project is as long as possible.
This means I don't want to be reliant on a server, subscription, or vendor.
If I can achieve this, I can host a project on GitHub Pages and it will be free to run forever.

## About WebRTC

WebRTC is all about peer-to-peer communication. The ideal is to have no server at all. This is not always possible, but it is the goal.

### Who do I connect to?

This is where signaling comes in.
Signaling is the process of coordinating peers to form the initial connection.
This can be done manually, though automated solutions require a signalling server.

### What is my public IP?

This is where STUN comes in.
STUN is a protocol that allows a client to obtain its public IP address.
Should you be connecting on the same network, this is not necessary.

### What if I am behind a NAT?

This is where TURN comes in.
TURN is a protocol that allows a client to relay data through a server.
This is a last resort, as it is not ideal for performance.

## References

- https://github.com/lesmana/webrtc-without-signaling-server
- https://developer.mozilla.org/en-US/docs/Web/API/RTCPeerConnection/createDataChannel
- https://github.com/feross/simple-peer?tab=readme-ov-file#data-channels
