This project demonstrates the impact of a Distributed Denial of Service (DDoS) attack on server infrastructure. The primary objective was to observe and document how a targeted flood of malicious traffic results in Resource Exhaustion, specifically focusing on CPU saturation and service unavailability. By simulating this environment on a private lab network, I analyzed the transition of a system from a healthy "Idle" state to a critical "Overload" state.

Technical Deep Dive: The "Before vs. After"
I monitored the system metrics in real-time using htop and nload to capture the following data points:

Baseline State (Normal Operation): With the Apache server hosting a modern e-commerce site, the system maintained a highly efficient baseline. CPU usage hovered between 2% – 3%, representing standard background processes and the idle web server daemon.

Attack State (Resource Exhaustion): Upon initiating a SYN Flood/UDP Stress test, the CPU utilization spiked immediately, fluctuating between 97% and 105%. This occurred because the CPU was forced to process an overwhelming number of interrupted handshakes, leaving no cycles available for legitimate user requests.
