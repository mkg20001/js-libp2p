# Peer and Content Routing

DHTs (Distributed Hash Tables) are one of the most common building blocks used when creating P2P networks. However, the name doesn't make justice to all the benefits it brings and putting the whole set of features in one box has proven to be limiting when we want to integrate multiple pieces together. With this in mind, we've come up with a new definition for what a DHT offers: Peer Routing and Content Routing.

Peer Routing is the category of modules that offer a way to find other peers in the network by intentionally issuing queries, iterative or recursive, until a Peer is found or the closest Peers, given the Peer Routing algorithm strategy are found.

Content Routing is the category of modules that offer a way to find where content lives in the network, it works in two steps: 1) Peers provide (announce) to the network that they are holders of specific content (multihashes) and 2) Peers issue queries to find where that content lives. A Content Routing mechanism could be as complex as a Kademlia DHT or a simple registry somewhere in the network.

# 1. Using Peer Routing to find other peers

This example builds on top of the Protocol and Stream Muxing. We need to install `libp2p-kad-dht`, go ahead and `npm install libp2p-kad-dht`.

`TODO`

# 2. Using Content Routing to find providers of content

`TODO`

# 3. Future Work

Currently, the only mechanisms for Peer and Content Routing come from the DHT, however we do have the intention to support:

- Multiple Peer Routing Mechanisms, including ones that do recursive searches (i.e webrtc-explorer like packet switching)
- Content Routing via PubSub
- Content Routing via centralized index (i.e a tracker)

