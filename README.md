# Cybersecurity Incident Report: Network Traffic Analysis

## Part 1: Provide a summary of the problem found in the DNS and ICMP traffic log.
![Screen Shot 2024-08-29 at 6 47 08 AM](https://github.com/user-attachments/assets/d9fa2f07-e7a0-4569-89fb-abadc3fca698)

---

|**Part 1: A summary of the problem found in the DNS and ICMP traffic log.**| Explanation      | 
|---------------------------------------------------------------------------|------------------|
|The network protocol analyzer logs indicate that port 53 is unreachable when trying to reach the DNS. The DNS seems to be overloaded and can’t send back the address of the client's website. This may indicate that there was a malicious attack on the DNS server that overloaded it with ICMP requests which created a denial of service D0S. The ICMP echo should have replied with the website address instead it returns an error message  UDP port 53 unreachable.”|- **A. Include a brief summary of the tcpdump log analysis and identify which protocols were used for the network traffic**. The scenario summarizes the issue and identifies the protocols used. Thescenario states: “To load the webpage, your browser first sends a query to a DNS server via the UDP protocol to retrieve the IP address for the website's domain name; this is part of the DNS protocol...The analyzer shows that when you send UDP packets to the DNS server, you receive ICMP packets containing the error message: “udp port 53 unreachable.” ” - B. **Provide a few details on what was indicated in the log.** The first and second step of the scenario section states that you performed a network analysis using tcpdump, which recorded UDP packets from your source computer to the IP address and port for the DNS server (203.0.113.2.domain). It also recorded the ICMP error responses from the DNS server back to your computer with the error message “udp port 53 unreachable.” We mention in the 6th step that “Port 53, is a port for DNS service,” which means this is an issue with the DNS server. We include further signs of issues with DNS performance in the fifth step of the scenario, “The plus sign after the query identification number indicates there are flags associated with the UDP message. The "A?" indicates a flag associated with|                                                                                                               

## Part 2: Explain your analysis of the data and provide at least one cause of the incident.

---

|**Part 2: Explain your analysis of the data and provide at least one cause of the incident.**                                                                               |
|-------------------------------------------------------------------------------------------------------------------------|
|In the afternoon, an incident occurred. The IT team encountered this incident when several clients reported that they were unable to reach the client's website due to an error. The team was tasked with investigating the issue. They loaded TCPDUMP, a network analyzer tool, and analyzed the network. Key findings from the IT department included the error message “port 53 unreachable” when sending an HTTPS request to the DNS. A likely cause of the incident is that the DNS received an abnormal amount of UDP protocol requests, overloading the system and causing a DoS.|



