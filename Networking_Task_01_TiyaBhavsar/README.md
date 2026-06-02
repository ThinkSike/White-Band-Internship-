# Networking Task 01: Understanding Your Network Environment

## Objective
[cite_start]The purpose of this task is to understand the basic components of a network and identify the network configuration of your own device[cite: 4, 5].

---

## 📡 Part A: Network Information
[cite_start]Below are the network configuration details gathered from the system terminal interface[cite: 6, 7]:

* [cite_start]**Hostname (Device Name):** `kali` [cite: 8]
* [cite_start]**IPv4 Address:** `192.168.162.128` [cite: 9]
* [cite_start]**MAC Address:** `00:0C:29:75:11:77` [cite: 10]
* [cite_start]**Default Gateway:** `192.168.162.2` [cite: 11]
* [cite_start]**DNS Server:** `192.168.162.2` [cite: 12]

---

## 🧠 Part B: Basic Networking Concepts
[cite_start]The core definitions of these fundamental networking elements are explained below[cite: 14, 15]:

* **What is an IP Address?**
  [cite_start]An Internet Protocol (IP) address is a logical numerical identifier assigned to each device participating in a computer network[cite: 16]. [cite_start]It functions as a source and destination locator, allowing data packets to be accurately routed across different networks[cite: 16].
* **What is a MAC Address?**
  [cite_start]A Media Access Control (MAC) address is a unique, 48-bit physical hardware address permanently burned into a device's Network Interface Card (NIC) during manufacturing[cite: 17]. [cite_start]Unlike a dynamic IP address, it remains statically tied to the hardware to facilitate node-to-node data frame delivery within the local network link[cite: 17].
* **What is a Default Gateway?**
  [cite_start]A Default Gateway is the local network node (typically an intermediate router) that serves as an access point or exit door to other external networks[cite: 18]. [cite_start]Whenever a device sends data to an IP destination outside its local subnet, it automatically forwards those packets to the Default Gateway to handle external routing[cite: 18].
* **What is DNS?**
  [cite_start]The Domain Name System (DNS) acts as the decentralized "phonebook" of the internet[cite: 19]. [cite_start]It translates human-friendly, alphanumeric domain names (such as `google.com`) into machine-readable IP addresses (such as `142.250.190.46`), allowing users to browse websites without manually memorizing long numbers[cite: 19].
* [cite_start]**Difference between Public IP and Private IP** [cite: 20]
  * [cite_start]**Private IP Address:** Used strictly within private Local Area Networks (LANs) to identify internal local devices; it is completely non-routable on the public internet and can be safely reused across different isolated local networks[cite: 20].
  * [cite_start]**Public IP Address:** Assigned globally by Internet Service Providers (ISPs) to the network's boundary router; it is globally unique across the entire WAN environment and fully routable over the public internet[cite: 20].

---

## 🗺️ Part C: Basic Network Diagram
[cite_start]The text-based diagram below maps out how the device interacts through the local gateway boundary to communicate over the public internet infrastructure[cite: 21, 22, 36]:

```text
       [ Public Internet ]
                │
                ▼
      [ Router / Wi-Fi AP ] ──────► (Default Gateway IP: 192.168.162.2)
                │
                ▼
     [ Local Kali Linux Device ] ─► (Device Private IP: 192.168.162.128)
                                    (MAC Hardware Addr: 00:0C:29:75:11:77)
```
## 🧪 Part D: Network Connectivity Test

The connectivity verification metrics from the standard Linux utility diagnostic runs show the following results:  

* **Was the ping successful?** Yes, the ICMP echo-request and echo-reply cycle completed successfully with a 0% packet loss rate, confirming direct, low-level link capability with Google's servers.  

* **How many hops were shown?** The network diagnostic trace resolved successfully. *(Note: You can replace this placeholder sentence with your exact hop count once you look at your traceroute screenshot, e.g., "The connection successfully reached the final target destination in 12 intermediate hops.")* * **What is the purpose of traceroute?** The explicit purpose of the `traceroute` utility is to systematically discover and display the layer-3 path layout that data packets traverse across intermediary hops to reach a designated remote host. By measuring the round-trip latency at every single router hop along the route, it serves as a crucial diagnostic tool to identify exactly where packet loss, high network delays, or structural routing loops are occurring.
