---
title: "CS610 – Exam Questions (Lectures 36–44)"
date: 2025-05-05 10:00:00 +0500
categories: [Networking, Exams]
tags: [TCP, NAT, Routing, OSPF, BGP, Multicast]
---

This post contains scenario-based exam-style questions drawn from Lectures 36 to 44 of the CS610 course. These questions are designed to reinforce core networking concepts and prepare you for assessments.

---

## 📘 Lecture 36 – TCP Segment Transmission

**Q1:**  
Events at Host A Events at Host B

send segment 1 ────────────────► receive segment 1
receive ACK 1 ◄─────────────── send ACK 1
send segment 2 ────────────────► receive segment 2
ACK 2 is lost
timeout occurs
retransmit segment 2 ─────────────► receive segment 2 again
receive ACK 2 ◄─────────────── send ACK 2 again

**Question:**  
Did Host A retransmit segment 2 because the segment itself was lost?

**Answer:**  
No, Host A retransmitted segment 2 because the **ACK for segment 2 was lost**, not the segment itself.

---

**Q2:**  
A sender can only transmit a limited number of segments before needing to wait for acknowledgments. What mechanism controls this flow?

**Answer:**  
The sender uses **TCP’s sliding window mechanism** to control data flow between the sender and receiver.

---

## 📗 Lecture 37 – NAT

**Q1:**  
A private IP `10.0.0.1` communicates with a public server. The router replaces this with `128.210.24.6` and translates responses back. What technique is being used?

**Answer:**  
**Network Address Translation (NAT).**

**Q2:**  
A device on `192.168.1.5` accesses a website. The server sees `203.0.113.5`. Which router mechanism makes this possible?

**Answer:**  
**NAT translates the private IP to the public IP** of the router.

---

## 📘 Lecture 38 – NAPT

**Q1:**  
A router translates both IPs and port numbers for multiple internal devices. What technique is used?

**Answer:**  
**Network Address Port Translation (NAPT).**

**Q2:**  
How do multiple home devices share one public IP?

**Answer:**  
Using **NAT**, all devices access the internet through a single public IP.

---

## 📗 Lecture 39 – Routing Basics

**Q1:**  
How does a router decide where to send a packet?

**Answer:**  
Using its **routing table** to determine the next hop.

**Q2:**  
What allows routers to exchange network reachability information?

**Answer:**  
**Routing protocols** like **RIP** and **OSPF**.

---

## 📘 Lecture 40 – Inter-Domain Routing

**Q1:**  
What protocol do ISPs use to exchange route information?

**Answer:**  
**Border Gateway Protocol (BGP).**

**Q2:**  
Which type of protocol routes traffic between an organization and ISP?

**Answer:**  
**Exterior Gateway Protocol (EGP)**, such as **BGP**.

---

## 📗 Lecture 41 – RIP and Redundancy

**Q1:**  
A distance-vector protocol updates every 30 seconds and limits hops to 15. Which protocol is this?

**Answer:**  
**RIP (Routing Information Protocol).**

**Q2:**  
How is outbound traffic handled when two ISPs are available?

**Answer:**  
**Routing protocols select the best path** based on policies and metrics.

---

## 📘 Lecture 42 – OSPF and BGP Behavior

**Q1:**  
Router R1 has two OSPF paths of equal cost to a destination. What will happen?

**Answer:**  
**OSPF load-balances traffic** across both equal-cost paths.

**Q2:**  
Which BGP route is preferred if one has a shorter AS path?

**Answer:**  
**The one with the shorter AS path**—considered more efficient.

---

## 📗 Lecture 43 – TTL and Multicast

**Q1:**  
What prevents packets from looping indefinitely?

**Answer:**  
**TTL (Time-to-Live)** field in the IP header.

**Q2:**  
How can one video stream be sent to many users efficiently?

**Answer:**  
Using **IP multicasting** to send one stream to multiple clients.

**Q3:**  
How is unnecessary multicast traffic avoided when no hosts are listening?

**Answer:**  
**IGMP** stops routers from forwarding multicast traffic when no listeners exist.

---

## 📘 Lecture 44 – Multicast Protocols

**Q1:**  
Which multicast protocol is based on RIP and avoids loops?

**Answer:**  
**DVMRP**, using reverse path forwarding.

**Q2:**  
Which protocol extends OSPF for multicast?

**Answer:**  
**MOSPF**, by including group data in LSAs.

**Q3:**  
Which transport protocol ensures reliable, ordered communication between two internet applications?

**Answer:**  
**TCP**, which guarantees reliability, ordering, and error checking.

---

📌 *These conceptual questions reinforce practical understanding of how networking protocols operate across different layers and scenarios.*

