# Cybersecurity Incident Report: Network Traffic Analysis

## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log.

---

**Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log.**

The UDP protocol reveals that port 53 is unreachable. This is based on the results of the network analysis, which show that the ICMP echo reply returned the error message “UDP port 53 unreachable.”

The port noted in the error message is used for the DNS server. The most likely issue is a DoS.

## Part 2: Explain your analysis of the data and provide at least one cause of the incident.

---

**Part 2: Explain your analysis of the data and provide at least one cause of the incident.**

In the afternoon, the IT team encountered this event when several clients reported that they were unable to reach the client's website due to an error.

The team was tasked with investigating the issue. They loaded TCPDUMP, a network analyzer tool, and analyzed the network.

Key findings from the IT department included the error message “port 53 unreachable” when sending an HTTPS request to the DNS. A likely cause of the incident is that the DNS received an abnormal amount of UDP protocol requests, overloading the system and causing a DoS.
