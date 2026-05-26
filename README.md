# PNL-for-Named-Data-Networking

An implementation of **Pending Interest Table (PIT) Lifetime Management (PNL)** or related predictive/neural-network-driven lifetime management strategies within **Named Data Networking (NDN)** architectures. 

This repository focuses on optimizing cache efficiency, reducing interest packet drops, and managing PIT timeouts dynamically using advanced logic or machine learning techniques.

---

## 📌 Overview

In Named Data Networking (NDN), the Pending Interest Table (PIT) keeps track of forwarded Interest packets waiting for matching Data packets. Setting a static PIT lifetime often leads to two major issues:
* **Too Short:** Valid interests time out prematurely, causing unnecessary retransmissions.
* **Too Long:** The PIT becomes bloated, leading to memory saturation and potential DDoS vulnerability (Interest Flooding Attacks).

**PNL (Predictive/PIT Network Lifetime)** introduces a dynamic mechanism to adaptively calculate and allocate the optimal lifetime for incoming Interests, maximizing throughput while minimizing PIT size footprint.

---

## 🚀 Features

* **Dynamic PIT Lifetime Allocation:** Moves away from static timers to smart, context-aware expiration times.
* **Network State Awareness:** Adapts to current Round Trip Times (RTT), hop counts, and congestion levels.
* **Simulation-Ready:** Pre-configured for seamless integration with popular NDN simulation frameworks (e.g., `ndnSIM`).
* **Performance Analytics:** In-built scripts to log PIT utilization, packet drop rates, and overall network throughput.

---

## 🛠️ Tech Stack & Prerequisites

Before setting up the project, ensure you have the following installed:

* **OS:** Linux (Ubuntu 20.04/22.04 recommended) or macOS
* **Simulator:** [ndnSIM v2.x](https://ndnsim.net/) (NS-3 based NDN simulator)
* **Language:** C++11/C++14 (for core ndnSIM modules)
* **Analysis Tools:** Python 3.x, Matplotlib, and Pandas (for data parsing and visualization)

---

## 📦 Installation & Setup

1. **Clone the repository** into your `ndnSIM/ns-3/src` or designated extensions directory:
   ```bash
   git clone [https://github.com/your-username/PNL-for-Names-Data-Networking.git](https://github.com/your-username/PNL-for-Names-Data-Networking.git) pnl-ndn
   cd pnl-ndn
