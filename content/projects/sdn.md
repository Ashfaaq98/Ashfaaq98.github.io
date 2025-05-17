+++
title = 'SDN-based Load Balancer for SOHO Environments 🌐⚖️'
date = 2022-01-08T00:00:00+05:30
draft = false
summary = "Development of an SDN-based load balancing algorithm that utilizes server bandwidth metrics, implemented on a POX controller and tested in Mininet and Raspberry Pi environments."
technologies = ["SDN", "Load Balancing", "POX Controller", "Python", "Mininet", "Raspberry Pi", "OpenFlow", "bwm-ng", "Shell Scripting", "Network Performance"]
+++

## Project Overview

This research project focuses on the development of a **Software Defined Network (SDN)** based load balancing algorithm tailored to enhance network performance, particularly in Small Office/Home Office (SOHO) environments. Traditional load balancers can be expensive and inflexible. This project proposes a cost-effective and scalable solution by implementing the load balancer as an application on an SDN controller.

The core idea is to distribute client requests to servers based on the **least bandwidth utilized by a server** at a given time.  This approach aims to optimize resource utilization and improve response times. The system is designed to gather server bandwidth information over a separate wireless network to avoid congesting the primary data links.

---

### 🧠 What It Does

-  **Distributes Network Traffic:** Implements a load balancing algorithm on an SDN controller (POX) to intelligently distribute incoming client requests across a cluster of servers.
-  **Optimizes Server Selection:** Selects the most suitable server by identifying the one with the least current bandwidth usage.
-  **Dynamic Bandwidth Monitoring:** Servers periodically report their bandwidth utilization to the SDN controller. 
-  **Reduces Management Traffic Overhead:** Proposes using a separate wireless network for transmitting server bandwidth data to the controller, preventing interference with client-server data traffic.
-  **Comparative Analysis:** The proposed algorithm's performance (response time) is evaluated against traditional random and round-robin load balancing algorithms.
-  **Versatile Implementation:** Tested in both an emulated environment (Mininet) and a physical setup using Raspberry Pi devices.

---

### 🧰 Technical Highlights

-   **Controller & Language:** The load balancing application is developed as a module for the **POX controller** using **Python**.
-   **Core Algorithm:**
    -   The `_pick_server` function within the POX module reads bandwidth values from a file.
    -   It parses these values, sorts them to find the server with the least bandwidth, and directs traffic accordingly.
    -   The `MemoryEntry` class helps in remembering flow states.
-   **Bandwidth Data Collection:**
    -   A shell script designed to run on servers listed in `/home/pi/serverlist`.
    -   Uses `ssh` to connect to each server and `bwm-ng` to capture network interface (`eth0`) bandwidth (specifically the 'out' rate).
    -   Appends the collected bandwidth data to a central file (`/home/pi/values`) for the controller to access.
-   **SDN Architecture:**
    -   Decouples the control plane (POX controller) from the data plane (OpenFlow-enabled switches).
    -   Clients and servers connect to an OpenFlow switch (e.g., Open vSwitch).
    -   The controller manages flow table entries in the switch to direct traffic.
-   **Testing Environments:**
    -    **Mininet Emulator:** Used for creating virtual networks with multiple hosts and switches for initial testing and development.
    -    **Raspberry Pi:** Implemented on Raspberry Pi devices, with one acting as an OpenFlow switch (running Open vSwitch) and others as hosts/servers, demonstrating real-world applicability.
-   **Network Setup for Bandwidth Reporting:** The design incorporates a separate wireless network for servers to transmit their bandwidth information to the POX controller, minimizing impact on the data network.
-   **Performance Metrics:** Primarily focused on response time under varying numbers of requests and server cluster sizes, compared against random and round-robin algorithms.

---

### 🔗 Explore the Project

- **GitHub Repository:** [SDN-based Load Balancing Algorithm](https://github.com/Ashfaaq98/SDN_POX_Controller-Load_Balancer)


