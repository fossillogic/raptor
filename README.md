<p align="center">
    <img src=".github/logo.png" alt="Stego Tool Logo" width="620"/>
</p>

### 🦖 A Command-Line Network Hunter by **Fossil Logic**

Raptor Tool is a high-performance **network analysis and operations utility** built for engineers, security professionals, and advanced users. It unifies network diagnostics, traffic inspection, reconnaissance, and testing into a single, aggressive and precise command-line interface.

From simple connectivity checks like `ping` to advanced capabilities like `sniff`, `map`, and `audit`, Raptor empowers users to **hunt, analyze, and control network environments** with speed and accuracy.

---

## Features

- **Connectivity testing** — Fast and flexible `ping` with advanced controls
- **Port and service scanning** — Discover open ports, services, and OS fingerprints
- **Route tracing and mapping** — Visualize packet paths and full network topologies
- **Packet capture and inspection** — Deep traffic analysis with filtering and decoding
- **DNS and metadata intelligence** — Resolve, trace, and harvest domain/network data
- **Real-time network monitoring** — Observe bandwidth usage and active connections
- **Packet crafting and injection** — Build and send custom network packets
- **Traffic forwarding and tunneling** — Relay connections with optional encryption
- **Load testing tools** — Simulate traffic and stress-test services
- **Security auditing** — Identify vulnerabilities and misconfigurations in networks

---

## **Why Choose Raptor Tool?**

Raptor Tool is built for those who need **speed, precision, and control** over their networks.

- **All-in-One Network Suite**: Replace tools like `ping`, `nmap`, `tcpdump`, `netcat`, and `traceroute` with one unified interface.
- **Aggressive & Efficient**: Designed for rapid diagnostics and deep inspection.
- **Advanced Capabilities**: Go beyond basic networking with packet crafting, topology mapping, and intelligence gathering.
- **Security-Oriented**: Built-in auditing and reconnaissance tools for defensive and offensive workflows.
- **Developer & Engineer Ready**: Powerful enough for professionals, simple enough for daily use.
- **Cross-Platform**: Works across Linux, macOS, and Windows.
- **Modern Architecture**: Built for extensibility and performance.

Raptor Tool is your **network predator**—fast, precise, and always on the hunt.

---

## **Prerequisites**

Ensure you have the following installed before starting:

- **Meson Build System**: This project relies on Meson. For installation instructions, visit the official [Meson website](https://mesonbuild.com/Getting-meson.html).

## **Setting Up Meson Build**

1. **Install Meson**:
    - Follow the installation guide on the [Meson website](https://mesonbuild.com/Getting-meson.html) for your operating system.

## **Setting Up, Compiling, Installing, and Running the Project**

1. **Clone the Repository**:

    ```sh
    git clone https://github.com/fossillogic/raptor.git
    cd raptor
    ```

2. **Configure the Build**:

    ```sh
    meson setup builddir
    ```

3. **Compile the Project**:

    ```sh
    meson compile -C builddir
    ```

4. **Install the Project**:

    ```sh
    meson install -C builddir
    ```

5. **Run the Project**:

    ```sh
    raptor --help
    ```

# 🦖 Raptor Tool — Network Command Palette

## Command Palette

---

### Network Operations

| **Command** | **Description** | **Flags** |
|-------------|-----------------|-----------|
| `ping` | Test reachability and latency to a host. | `--count <n>`<br>`--interval <ms>`<br>`--timeout <ms>`<br>`--size <bytes>`<br>`--flood`<br>`--ttl <n>` |
| `scan` | Scan ports and services on a target. | `--ports <range>`<br>`--fast`<br>`--service` (detect services)<br>`--os` (OS fingerprinting)<br>`--udp`<br>`--tcp`<br>`--timeout <ms>` |
| `track` | Trace packet path to a target (enhanced traceroute). | `--hops <n>`<br>`--resolve`<br>`--timeout <ms>`<br>`--geo`<br>`--graph`<br>`--protocol <type>` |
| `sniff` | Capture and inspect live network traffic. | `--iface <name>`<br>`--filter <expr>`<br>`--raw`<br>`--decode`<br>`--count <n>`<br>`--save <file>` |
| `resolve` | Perform DNS lookups and analysis. | `--type <record>`<br>`--reverse`<br>`--trace`<br>`--server <ip>`<br>`--cache` |
| `probe` | Check service availability and behavior. | `--port <n>`<br>`--service <name>`<br>`--banner`<br>`--tls`<br>`--timeout <ms>` |
| `harvest` | Collect metadata about a host or domain. | `--whois`<br>`--dns`<br>`--headers`<br>`--cert`<br>`--all` |
| `watch` | Monitor network activity in real-time. | `--iface <name>`<br>`--interval <n>`<br>`--top`<br>`--proto <type>`<br>`--threshold <rate>` |
| `inject` | Send crafted packets to a target. | `--target <ip>`<br>`--port <n>`<br>`--payload <data>`<br>`--protocol <type>`<br>`--repeat <n>` |
| `relay` | Forward traffic between endpoints. | `--listen <port>`<br>`--forward <host:port>`<br>`--protocol <type>`<br>`--encrypt`<br>`--log` |
| `cloak` | Mask or alter network identity. | `--spoof-ip <ip>`<br>`--mac <addr>`<br>`--randomize`<br>`--tor`<br>`--vpn <config>` |
| `burst` | Perform controlled load testing. | `--target <host>`<br>`--port <n>`<br>`--rate <req/s>`<br>`--duration <s>`<br>`--protocol <type>` |
| `map` | Build a network topology map. | `--range <cidr>`<br>`--discover`<br>`--services`<br>`--os`<br>`--graph` |
| `listen` | Open a listening socket. | `--port <n>`<br>`--protocol <type>`<br>`--exec <cmd>`<br>`--keep-alive` |
| `forge` | Craft custom packets manually. | `--ip <src/dst>`<br>`--tcp-flags <flags>`<br>`--payload <data>`<br>`--checksum` |
| `sync` | Synchronize data across network nodes. | `--source <path>`<br>`--dest <host:path>`<br>`--compress`<br>`--encrypt`<br>`--delta` |
| `audit` | Perform network security checks. | `--target <host>`<br>`--ports <range>`<br>`--vuln`<br>`--config`<br>`--report <file>` |

---

### Global Flags

| **Flag** | **Description** |
|-----------|-----------------|
| `--help` | Show command help. |
| `--version` | Display Spino Tool version. |
| `-v, --verbose` | Enable detailed output. |
| `-q, --quiet` | Suppress standard output. |
| `--dry-run` | Simulate actions without changes. |
| `--color` | Colorize output where applicable. |
| `--time` | Display timestamps in output. |

---

### Usage Examples

| **Example** | **Description** |
|---|---|
| `raptor ping --count 4 example.com` | Send 4 ping requests to a host. |
| `raptor scan --ports 1-1000 --service example.com` | Scan common ports and detect services. |
| `raptor track --geo --graph example.com` | Trace route with geolocation and visualization. |
| `raptor sniff --iface eth0 --filter "tcp port 80"` | Capture HTTP traffic. |
| `raptor resolve --type MX example.com` | Lookup mail server DNS records. |
| `raptor probe --service http --banner example.com` | Check HTTP service and grab banner. |
| `raptor harvest --all example.com` | Gather full domain intelligence. |
| `raptor watch --top --interval 2` | Monitor top bandwidth users. |
| `raptor map --range 192.168.1.0/24 --graph` | Visualize local network topology. |
| `raptor relay --listen 8080 --forward target:80` | Forward traffic to another host. |
| `raptor burst --target example.com --rate 100 --duration 10` | Run controlled load test. |
| `raptor audit --target example.com --vuln` | Run vulnerability checks. |

---

## **Contributing**

Interested in contributing? Please open pull requests or create issues on the [GitHub repository](https://github.com/fossillogic/raptor).

## **Feedback and Support**

For issues, questions, or feedback, open an issue on the [GitHub repository](https://github.com/fossillogic/raptor/issues).

## **License**

This project is licensed under the [Apache Public License](LICENSE).
