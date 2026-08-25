## Raul Fonseca

I write systems software, mostly C++. Engines, virtual machines, runtimes, and
firmware for small distributed clusters.

The projects below started as questions about how a layer works, and I answered
them by building that layer and then building the tooling to test it.

### Selected work

**[superposition](https://github.com/RaulFonseca002/superposition)**
A 3D engine with its own entity-component-system, an OpenGL renderer, and Bullet
physics. Each entity carries a 32-bit signature marking the components it holds,
and systems keep the set of entities whose signature matches theirs, so a
component being added updates one bitset and one set membership.

**[esp32-distributed-worker](https://github.com/RaulFonseca002/esp32-distributed-worker)**
Firmware for a cluster of ESP32-C3 nodes that share image-processing work. Nodes
elect a leader by MAC-derived id, the leader routes incoming frames by comparing
its own queue depth against each worker's heartbeat, and frames arrive over UDP
in chunks. Ships with Python tools that stand in for the camera and for extra
nodes, so the cluster can be exercised without the hardware.

**[bytecode-vm](https://github.com/RaulFonseca002/bytecode-vm)**
A stack machine with a two-pass loader that resolves labels and variables into
concrete addresses before execution. Ten programs under `TESTS/` run against
committed expected output, covering division by zero, stack overflow and
underflow, and signed 32-bit overflow.

**[n8n-randomorg-node](https://github.com/RaulFonseca002/n8n-randomorg-node)**
A custom n8n node in TypeScript that pulls random numbers from the Random.org
API, running in Docker against PostgreSQL. Built to someone else's specification.
