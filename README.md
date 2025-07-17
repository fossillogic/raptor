🦖 # *Raptor Tool*

Raptor is a lightning-fast, all-in-one command-line tool for networking, diagnostics, and security auditing. Built for system administrators, DevOps engineers, and terminal power users, Raptor centralizes everything you need to inspect, test, and secure your network.

Instead of juggling tools like ping, traceroute, netstat, tcpdump, nmap, and more, Raptor unifies these capabilities into one intuitive interface. Whether you’re tracing a route, scanning ports, checking DNS records, sniffing packets, analyzing connections, or locking down firewalls—Raptor delivers agile, high-performance diagnostics and network control from the command line.

With smart commands, layered sub-flags, and a modular structure, Raptor streamlines your network workflows with precision. Built for speed. Tuned for stealth. Engineered for security.

⸻

🔧 ## Global Flags

| **Flag**           | **Description**                             |
|--------------------|---------------------------------------------|
| `raptor --help`    | Display help information.                   |
| `raptor --version` | Display the current version of Raptor.      |
| `raptor --verbose` | Enable detailed output for all commands.    |

⸻

🧪 ## Commands

| **Command**       | **Flags**                                                                 | **Description**                                                                 |
|-------------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| `raptor ping`     | `--count=<n>`, `--timeout=<ms>`                                            | Ping a host and measure latency.                                               |
| `raptor trace`    | `--protocol=icmp\|udp\|tcp`, `--hops=<max>`                               | Trace network path to a target using various protocols.                        |
| `raptor scan`     | `--ports=1-65535`, `--target=<ip>`, `--stealth`, `--top`, `--udp`         | Scan for open TCP/UDP ports with advanced filtering.                           |
| `raptor dns`      | `--server=<dns>`, `--type=A\|AAAA\|MX\|TXT`, `--trace`, `--sec`           | Perform DNS lookups and trace resolution paths.                                |
| `raptor ssl`      | `--check=<host>`, `--expiry`, `--fullchain`, `--insecure`                 | Check SSL/TLS certificate validity, expiration, and chain.                     |
| `raptor netstat`  | `--open`, `--listening`, `--established`, `--programs`                    | Display active network sockets and connections.                                |
| `raptor sniff`    | `--interface=eth0`, `--filter=<expr>`, `--limit=<n>`, `--output=<file>`   | Capture and inspect network packets in real time.                              |
| `raptor detect`   | `--dns-leak`, `--public-ip`, `--rogue-dhcp`, `--promisc`                  | Run security tests and detect common misconfigurations.                        |
| `raptor firewall` | `--status`, `--enable`, `--disable`, `--allow <port>`, `--deny <ip>`      | Manage and inspect firewall rules.                                             |
| `raptor iface`    | `--list`, `--up`, `--down`, `--stats`, `--rename <new>`                   | Monitor and control network interfaces.                                        |
| `raptor route`    | `--table`, `--default`, `--add`, `--del`                                  | Inspect and modify the routing table.                                          |
| `raptor proxy`    | `--set`, `--clear`, `--status`                                            | Manage proxy environment configurations.                                       |
| `raptor secure`   | `--scan`, `--ssh`, `--certs`, `--ports`, `--summary`                      | Run security audits across services, keys, and configurations.                 |
| `raptor monitor`  | `--threshold`, `--notify`, `--log`                                        | Monitor networking events and usage patterns.                                  |
| `raptor test`     | `--ssl`, `--dns`, `--http`, `--connectivity`                              | Run quick service tests for web and DNS targets.                               |

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
    raptor
    ```

## **Contributing**

Interested in contributing? Please open pull requests or create issues on the [GitHub repository](https://github.com/fossillogic/raptor).

## **Feedback and Support**

For issues, questions, or feedback, open an issue on the [GitHub repository](https://github.com/fossillogic/raptor/issues).

## **License**

This project is licensed under the [Mozilla Public License](LICENSE).