+++
title = "Model Context Protocol (MCP) Servers for Cyber 🧩"
date = 2025-04-05T00:00:00+01:00
draft = false
summary = "A Langgraph CTI agent that leverages a MCP client to connect to MCP Servers"
technologies = ["Python","Langgraph","Model Context Protocol", "RSTCloud", "VirusTotal","Smithery","Alient Vault OTX"]
+++

## 🧠 Project Overview

This repository provides a modular collection of **MCP (Model Context Protocol) servers** for cybersecurity threat intelligence (CTI) applications. Each server integrates with a third-party CTI provider and exposes structured threat data to LangGraph-based agents via a standardized MCP interface.

The goal is to **enable real-time, contextual intelligence gathering** through seamless plug-and-play server modules.

---

### 🧪 Implemented Servers

1. **🔬 VirusTotal**  
   Connects to the VirusTotal API to retrieve threat reports on:
   - File hashes, domains, IPs, and URLs  
   - Threat categories and metadata  
   - Mapped MITRE ATT&CK tactics and techniques  

2. **🛰️ RSTCloud**  
   Leverages the RSTCloud API to deliver real-time intelligence with:
   - IOC enrichment (IPs, hashes, domains, URLs)  
   - Threat classification and contextual metadata  
   - Linked attack vectors and behavioral patterns  

3. **🛡️ AlienVault OTX**  
   Integrates with the AlienVault Open Threat Exchange to:
   - Query threat pulses and community-contributed indicators  
   - Retrieve associated file hashes, IPs, and domains  
   - Access attack tags, tags, techniques, and contributor metadata  

---


### 🔗 Explore the Repository

- **GitHub Repository:** [priamai/mcp](https://github.com/priamai/mcp)

---