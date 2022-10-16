# Client-Server Architecture
Client-server architecture, alternatively called a client-server model, is a network application that breaks down tasks and workloads between clients and servers that reside on the same system or are linked by a computer network.

Client-server architecture typically features multiple users’ workstations, PCs, or other devices, connected to a central server via an Internet connection or other network. The client sends a request for data, and the server accepts and accommodates the request, sending the data packets back to the user who needs them.

This model is also called a client-server network or a network computing model.

To sum it up briefly:

First, the client sends their request via a network-enabled device
Then, the network server accepts and processes the user request
Finally, the server delivers the reply to the client

## The Characteristics of Client-Server Architecture
Client-server architecture typically features the following characteristics:

Client and server machines typically require different hardware and software resources and come from other vendors.
The network has horizontal scalability, which increases the number of client machines and vertical scalability, an then moves the entire process to more powerful servers or a multi-server configuration.
One computer server can provide multiple services simultaneously, although each service requires a separate server program.
Both client and server applications interact directly with a transport layer protocol. This process establishes communication and enables the entities to send and receive information.
Both the client and server computers need a complete stack of protocols. The transport protocol employs lower-layer protocols to send and receive individual messages.

## Visualizing Client-Server Architecture
The following client-server diagram shows the basics of of the architecture:
![client-server architecture](https://www.simplilearn.com/ice9/free_resources_article_thumb/Client_Server_Architecture_1.png)

## Advantages of Client-Server Architecture:
1. Centralized system with all data in a single place.
2. Cost efficient requires less maintenance cost and Data recovery is possible.
3. The capacity of the Client and Servers can be changed separately.

## Disadvantages of Client-Server Architecture:
1. Clients are prone to viruses, Trojans and worms if present in the Server or uploaded into the Server.
2. Server are prone to Denial of Service (DOS) attacks.
3. Data packets may be spoofed or modified during transmission.
4. Phishing or capturing login credentials or other useful information of the user are common and MITM(Man in the Middle) attacks are common.


