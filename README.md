## Raul Fonseca

I build the layer underneath — engines, virtual machines, runtimes, and embedded
clusters, mostly in C++.

Most of these started as a question about how something works and ended as an
implementation of it. The pattern I keep repeating is building the substrate
first, then building the tools to test it.

### Selected work

**[superposition](https://github.com/RaulFonseca002/superposition)** — a 3D engine
written from scratch: its own entity-component-system with bitset signature
matching, an OpenGL renderer, and Bullet physics. Entities are matched to systems
by a single machine-word comparison.

**[esp32-distributed-worker](https://github.com/RaulFonseca002/esp32-distributed-worker)** —
firmware for a self-organizing cluster of ESP32-C3 nodes that share
image-processing work. Bully leader election, load balancing by queue depth, and
a chunked-UDP frame protocol documented for the team building the camera node.
Ships with host-side tools that simulate the cluster without hardware.

**[bytecode-vm](https://github.com/RaulFonseca002/bytecode-vm)** — a stack-based
virtual machine with a loader, an IR stage, and a ten-case golden-file regression
suite covering the failure modes: division by zero, stack overflow and underflow,
signed overflow.

**[n8n-randomorg-node](https://github.com/RaulFonseca002/n8n-randomorg-node)** — a
custom n8n node in TypeScript integrating the Random.org API, containerized with
Docker and PostgreSQL. Built to someone else's spec.
