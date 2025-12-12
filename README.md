*This project has been created as part of the 42 curriculum by ria-ded.*

# 🌐 Network Routing Trainer: NetPractice

## 📝 Description

This project serves as a practical, hands-on training exercise to master the foundational concepts of modern computer networking, specifically focusing on **Layer 3 (Network Layer)** operations.

The **goal** of this project is to successfully configure a series of increasingly complex network topologies to ensure end-to-end connectivity between various host machines, routers, and external networks (simulated Internet). Success is measured by correctly implementing **static routing** logic, appropriate **subnetting**, and configuring device-level settings (like default gateways) to solve connectivity challenges across different subnets and network segments. The project requires the application of fundamental TCP/IP addressing principles to design and implement robust, multi-router networks.

## 🛠️ Instructions

### 1. Execution

The project utilizes a custom or simulated training interface, which is the primary tool for solving the challenges.

To start the training interface:
* Download the file attached to the project’s page: **net_practice.1.7**.
* Extract the files in whatever folder you want.
* In this folder, run the index.html file.
* This interface should open in your web browser.
* The interface will present a series of 10 network configuration challenges.

### 2. Configuration & Export

For each challenge (or "level"), you must successfully configure all hosts and routers to achieve the stated connectivity goal.

**To export your final, working configuration for submission:**
1.  In the simulation interface, locate the **[Get my config]** button.
2.  Export the configuration file for the current level.

### 3. Submission Details

The final submission requires placing all necessary files at the root of the repository.

* **Exported Configurations:** **Ten (10)** exported configuration files (one per training level) must be placed directly at the repository root. (e.g., `level1.json` through `level10.json`).
* A README.md file must be provided at the root of Git repository.

_Original source files should not be included._

## 📌 Routing Essentials
* **Segmentation**: Every link/LAN is a unique, non-overlapping subnet.
* **Rule:** Router connects different subnets. Switch connects hosts in the same subnet.
* **Addressing:** All IPs in a local network share the exact same subnet mask.
  - Sizing: To broaden (more hosts), reduce the mask number (e.g., $/25 \rightarrow /24$).
  - Caution: Do not use the Network ID (first IP) or Broadcast Address (last IP).
* Host Default: A host's gateway is the IP of the router interface on its local subnet.
* **Routing Table:** Shows "To reach $\text{[Destination Network]}$, go to $\text{[Next Hop IP]}$."
  - Next Hop: The $\text{Next Hop IP}$ is always a neighboring router's interface IP.
* **Router Knowledge:** Routers auto-learn Directly Connected networks. Remote networks must be added manually (Static Routes).
* **Prioritization:** Routers use Longest Prefix Match (LPM): The most specific route (longest mask) is always chosen over a broader one ($0.0.0.0/0$).
* **External Access:** For the outside world (Internet) to respond, its router must have a route to your internal network. Private IPs require NAT at the border.


## 📚 Resources

This project heavily relies on the following networking concepts **Networking Concepts Studied**:

* **TCP/IP Addressing:** Understanding IPv4 addresses, address classes, and private vs. public ranges.
* **Subnet Mask (CIDR):** Calculating network and broadcast addresses, determining usable host ranges, and performing Variable Length Subnet Masking (VLSM).
* **Default Gateway:** The function of the router interface as the exit point for hosts reaching remote networks.
* **Routers and Switches:** Differentiating between Layer 2 (switching) and Layer 3 (routing) devices and their roles in data forwarding.
* **Routing Table:** The structure and function of the routing information base, including Direct, Static, and Default routes.
* **Longest Prefix Match (LPM):** The mechanism routers use to prioritize specific routes over broad ones (e.g., a $/30$ route over a $0.0.0.0/0$ default).
* **OSI Layers:** Focus on Layers 1 (Physical), 2 (Data Link), and 3 (Network) and how devices operate at each layer.

### References

* [Cisco CCNA Official Certification Guide](https://learningnetwork.cisco.com/s/learning-plan-detail-standard?ltui__urlRecordId=a1c3i0000005dy7AAA&ltui__urlRedirect=learning-plan-detail-standard&utm_campaign=ccnacertguide&utm_source=certguide&utm_medium=cisco-learning-network)
* [Cisco CCNA 200-301](https://www.youtube.com/watch?v=LIzTo6e4FgY)
* [Free CCNA | Network Devices | Day 1 | CCNA 200-301 Complete Course](https://youtu.be/H8W9oMNSuwo?si=fCesM3j-QgsPI29y)

### AI Usage

In the development and documentation of this project, I utilized a Large Language Model (LLM) as an intelligent assistant for the **Conceptual Clarification**:
The AI was used to critically evaluate and challenge my understanding of complex topics, such as the difference between a default route and a static route, and the specific behavior of the Longest Prefix Match algorithm.
