# Infinity - RDMA High-Performance Communication Research

## 🎯 My Personal Exploration & Research
**This repository serves as my hands-on laboratory for studying high-performance networking and system programming.** As part of my preparation for software engineering roles in AI infrastructure (specifically focusing on technologies like NVIDIA Spectrum-X), I am using this project to explore:

* **Kernel Bypass:** Understanding how to transfer data without involving the OS kernel to reduce latency.
* **Zero-Copy Architecture:** Moving data directly from application memory to the network card (NIC).
* **C++ Memory Management:** Learning about memory pinning and registered memory regions.



---

## 🏗 About Infinity (Original Project)
Infinity is a high-level C++ library for RDMA (Remote Direct Memory Access). It provides an object-oriented interface to the `ibverbs` library, making it easier to build high-performance distributed systems.

### Key Features
* Easy-to-use abstractions for Queue Pairs, Memory Regions, and Completion Queues.
* Support for Two-Sided (Send/Receive) and One-Sided (Read/Write/Atomic) operations.
* Built-in connection management.

## 🔍 Code Analysis Highlights
I have analyzed the following core components to understand the RDMA workflow:
* **`src/infinity/core/Context.cpp`**: Understanding how the RDMA environment is initialized.
* **`src/infinity/queues/QueuePair.cpp`**: Researching how connections are established between nodes.
* **`src/examples/read-write-send.cpp`**: Analyzing the performance difference between one-sided and two-sided operations.

## 🛠 Requirements
The following packages are required for building the library:
* `libibverbs-dev`
* `cmake` (version 2.8 or higher)
* A C++11 compliant compiler (e.g., `g++` 4.8 or higher)

## 🚀 Building and Running
1. **Clone and Build:**
   ```bash
   mkdir build && cd build
   cmake ..
   make
