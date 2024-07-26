Scenery

Analyze the following case. Then, complete the instructions step by step.

You are a cybersecurity analyst working at a company that specializes in providing computer consulting services. Several customers contacted your company to report that they could not access the company website www.yummyrecipesforme.com, and saw the “destination port unreachable” error after waiting for the page to load.

You are tasked with analyzing the situation and determining which network protocol was affected during this incident. To begin with, you visit the website and also get the “destination port unreachable” error. Next, you load your network analysis tool, tcpdump, and reload the web page. This time, you receive a large number of packets on your network analyzer. The analyzer shows that when you send UDP packets and receive an ICMP response returned to your host, the results contain an error message: “udp port 53 unreachable.” (udp port 53 unreachable).

In the DNS and ICMP record, you find the following information:

In the first two lines of the log file, you see the initial outgoing request from your computer to the DNS server requesting the IP address of yummyrecipesforme.com. This request is sent in a UDP packet.

Below you will find timestamps indicating when the event occurred. In the registry, this is the first sequence of numbers displayed. For example: 13:24:32.192571. This shows the time 1:24 p.m. m., 32.192571 seconds.

The following is the source and destination IP address. In the error log, this information is displayed as: 192.51.100.15.52444 > 203.0.113.2.domain. The IP address to the left of the greater than symbol (>) is the source address. In this example, the source is your computer's IP address. The IP address to the right of the greater than symbol (>) is the destination IP address. In this case, it is the IP address of the DNS server: 203.0.113.2.domain

The second and third lines of the log show the response to your initial ICMP request packet. In this case, the ICMP line 203.0.113.2 is the beginning of the error message indicating that the ICMP packet could not be delivered on the DNS server port.

Next are the protocol and port number, which shows which protocol was used to handle communications and which port it was delivered to. In the error log, this appears as “udp port 53 unreachable.” This means that the UDP protocol was used to request domain name resolution using the DNS server address over port 53. Port 53, which aligns with the .domain extension at 203.0.113.2.domain, is a port well known for DNS service. The word “unreachable” in the message indicates that the message did not reach the DNS server. Your browser could not obtain the IP address of yummyrecipesforme.com, which it needs to access the website because no service was listening on the receiving DNS port, as indicated by the ICMP error message “udp port 53 unreachable.” (udp port 53 unreachable).

The remaining lines of the log indicate that ICMP packets were sent two more times, but the same delivery error was received both times.

Now that you have captured data packets using a network analysis tool, your job is to identify which protocol and network service were affected by this incident. Then, you will have to write a monitoring report.

As an analyst, you can inspect network traffic and network data to determine what is causing network-related issues during cybersecurity incidents. Later in this course, you will demonstrate how to manage and resolve incidents. For now, you just need to analyze the situation.

In the meantime, this incident is being handled by security engineers after you and other analysts have reported the issue to your direct supervisor.
