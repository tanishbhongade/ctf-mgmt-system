# Distributed CTF Management System

This system is designed to facilitate Capture The Flag (CTF) competitions by providing a distributed architecture that ensures high scalability, player isolation, and minimized cheating.

## Architecture Overview

The system comprises four main components:

1. **CTF Management Server**  
   The central authority that manages player registrations, tracks player states, and coordinates with worker nodes to allocate isolated environments.

2. **CTF Worker Node**  
   Each worker node is responsible for creating and managing isolated containers for players, ensuring resource allocation and environment isolation.

3. **CTF Frontend**  
   The user interface through which participants interact with the system, register for competitions, and access their isolated environments.

4. **CTF SSH Proxy Server**  
   Acts as an intermediary to securely proxy SSH connections from the frontend to the player's container environment.

## GitHub Repositories

You can access and contribute to each component via the following GitHub repositories:

- [CTF Management Server](https://github.com/tanishbhongade/ctf-mgmt-server)
- [CTF Worker Node](https://github.com/tanishbhongade/ctf-workernode)
- [CTF Frontend](https://github.com/tanishbhongade/ctf-frontend)
- [CTF SSH Proxy Server](https://github.com/tanishbhongade/ctf-ssh-proxy-server)

## Medium Article

For a detailed explanation of the system's architecture and design decisions, refer to the following article:

- [Distributed CTF Management System](https://medium.com/@tanishbhongade/distributed-ctf-management-system-47395c842f37)

## Features

- **Horizontal Scalability**: Utilizes a round-robin algorithm to distribute player load across multiple worker nodes.
- **Player Isolation**: Each player operates within a Docker container, ensuring a secure and isolated environment.
- **Authentication and Security**: Employs HMAC for secure communication between the management server and worker nodes, and JWT tokens for seamless frontend-backend interaction.
- **Real-time Interaction**: Enables real-time SSH access to player environments through the SSH proxy server.

## Installation and Setup

For detailed instructions on setting up each component, please refer to the README files within each respective repository.
