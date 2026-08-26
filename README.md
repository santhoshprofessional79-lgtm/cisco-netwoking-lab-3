# 🚀 SOC Analyst Network Foundations: Lab 3 (VLANs & Trunking)

Welcome to Lab 3! In this simulation, I focused on a critical security control used in enterprise environments: **Network Segmentation**. By implementing Virtual LANs (VLANs) and Trunking across multiple switches, I established logical isolation within a physical network.

 🛠️ Tools Used
* Cisco Packet Tracer (CLI Configuration)
* Switch IOS Commands (VLAN, Access Ports, 802.1Q Trunking)

---

 📸 Lab Workflow & Configuration

 1. VLAN Creation & Access Ports (Isolation)
Action: Configured VLAN 10 (IT) and VLAN 20 (HR) on a Cisco Switch. Assigned specific switch ports to these VLANs (Access Mode).
Result: Successfully isolated broadcast domains. Demonstrated that PCs in VLAN 10 cannot ping PCs in VLAN 20, even though they are connected to the exact same physical switch. 

 2. Switch-to-Switch Trunking (802.1Q)
Action: Expanded the topology by adding a second switch. Configured a Trunk Link (Gig0/1) between the switches to carry traffic for multiple VLANs simultaneously.
Result: Verified that IT PCs on Switch 1 can successfully communicate with IT PCs on Switch 2 via the trunk link, while maintaining strict isolation from the HR department.

---

 🛡️ SOC & Security Takeaways
Preventing Lateral Movement:  In a SOC environment, flat networks are highly vulnerable. If an attacker compromises a machine in the HR department, VLAN segmentation prevents them from easily scanning or pivoting to critical IT servers.
Blast Radius Reduction: By logically separating departments, we contain malware outbreaks (like ransomware) to a single VLAN, severely limiting the "blast radius" of an incident.
