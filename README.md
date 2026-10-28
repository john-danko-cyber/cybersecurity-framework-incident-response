# Using the Cybersecurity Framework to Respond to a Security Incident

## Summary
A guided course lab in which I analyzed a provided scenario for a multimedia company whose network was knocked offline for two hours by a denial of service (DoS) attack. A flood of ICMP packets came in through a firewall that was not configured to limit ICMP traffic. I applied the five core functions of the NIST Cybersecurity Framework (CSF), Identify, Protect, Detect, Respond, and Recover, to analyze the incident and wrote an incident report recommending how the company can prevent, detect, respond to, and recover from similar attacks.

## My Role
I analyzed the provided scenario, mapped the incident and the security team's response to each NIST CSF function, and wrote the incident report analysis. The scenario, the NIST CSF reference guide, and the incident report template were provided by the course lab.

## Project Overview

This project documents a guided lab from the Google Cybersecurity Certificate. The lab provides a scenario about a cybersecurity incident, a reference guide to the NIST CSF and its five core functions, and an incident report analysis template. I used the questions for each function in the guide to break down what was affected, what safeguards were missing, how the attack could be detected, and how the team should respond and recover.

The report recommends maintaining firewall configurations, rate limiting incoming ICMP packets, verifying source IP addresses to catch spoofed packets, adding network monitoring software, and using an IDS/IPS to filter suspicious ICMP traffic, along with a written response and recovery plan.

---

## Scenario

A multimedia company that offers web design, graphic design, and social media marketing services to small businesses suddenly lost all network services. The incident management team found that a flood of incoming ICMP packets had overwhelmed the internal network, so normal traffic could not reach any network resources.

The team responded by blocking incoming ICMP packets, stopping all non-critical network services, and restoring critical network services. The network was down for two hours. An investigation found that the attacker sent the ICMP flood through a firewall that had not been configured to limit ICMP traffic.

To address the event, the network security team put in place:

1. A new firewall rule to limit the rate of incoming ICMP packets.
2. Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets.
3. Network monitoring software to detect abnormal traffic patterns.
4. An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics.

My part was to write an incident report analysis that applies the NIST CSF to this event.

---

## Tools Used

- NIST Cybersecurity Framework (CSF) reference guide provided in the lab
- Google Cybersecurity Certificate incident report analysis template

---

## Key Findings

- **Root cause:** the firewall was not configured to limit ICMP traffic, so the attacker could send an ICMP flood straight into the internal network.
- **Impact:** network services were unavailable for two hours, and the company could not carry out its normal client work in web design, graphic design, and social media marketing.
- **Initial response:** blocking incoming ICMP packets, stopping non-critical services, and restoring critical services first brought the network back under control.
- **Detection gap:** there was no monitoring in place to alert the team to abnormal traffic before services went down.
- **Overall risk:** without firewall rules, spoofing checks, and monitoring, the company stays open to the same kind of denial of service attack.

---

## NIST CSF Breakdown

| Function | Focus in this incident |
|---|---|
| Identify | Unconfigured firewall, affected network services and business processes, and who needs access |
| Protect | Firewall maintenance, ICMP rate limiting, source IP verification, IDS/IPS, and access control |
| Detect | Network monitoring software, IDS/IPS alerts, firewall logs, and a SIEM |
| Respond | DoS response plan, communication with IT staff and end users, log analysis, and mitigation |
| Recover | Restoring critical services first, then non-critical services, and confirming normal operation |

Full explanations are in the incident report analysis.

---

## Project Documentation

### [Incident Report Analysis](incident-report-analysis.md)
The completed incident report analysis covering the summary of the event and each of the five NIST CSF functions.

---

## Skills Demonstrated

- Applying the NIST Cybersecurity Framework to a real-world style incident
- Analyzing a DoS attack (ICMP flood) and tracing its root cause
- Recommending firewall rules, source IP verification, monitoring, and IDS/IPS controls
- Planning incident response, communication, and recovery steps
- Incident report documentation

---

## What I Learned

- A single firewall misconfiguration can take down an entire network, even without any data being stolen.
- The NIST CSF gives a clear structure for looking at an incident before, during, and after it happens.
- Detection matters as much as prevention, because monitoring and IDS/IPS alerts can catch abnormal traffic before services go down.
- Restoring critical services first keeps the business running while the rest of the network is brought back.

---

## Disclaimer

This is a guided lab completed as part of the Google Cybersecurity Certificate. The organization and the incident are part of a training scenario, not a real production environment.

This project is based on a scenario from the Google Cybersecurity Professional Certificate (Coursera). The write-up and analysis are my own.

## Evidence
- [Incident Report Analysis](incident-report-analysis.md)
- [NIST CSF Breakdown](#nist-csf-breakdown) (summary table of each function)
