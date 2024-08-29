# Cybersecurity Incident Report: Network Traffic Analysis

## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log.
![Screen Shot 2024-08-29 at 6 47 08 AM](https://github.com/user-attachments/assets/d9fa2f07-e7a0-4569-89fb-abadc3fca698)

---

**Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log.**

The network protocol analyzer logs indicate that port 53 is unreachable when trying to reach the DNS. The DNS seems to be overloaded and can’t send back the address of the client's website. This may indicate that there was a malicious attack on the DNS server that overloaded it with ICMP request which created a denial of service D0S. The ICMP echo should of reply with the website address instead it returns an error message  UDP port 53 unreachable”.

## Part 2: Explain your analysis of the data and provide at least one cause of the incident.

---

**Part 2: Explain your analysis of the data and provide at least one cause of the incident.**

In the afternoon, an incident occurred. The IT team encountered this incident when several clients reported that they were unable to reach the client's website due to an error.

The team was tasked with investigating the issue. They loaded TCPDUMP, a network analyzer tool, and analyzed the network.

Key findings from the IT department included the error message “port 53 unreachable” when sending an HTTPS request to the DNS. A likely cause of the incident is that the DNS received an abnormal amount of UDP protocol requests, overloading the system and causing a DoS.



