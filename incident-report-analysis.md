# Incident Report Analysis: Multimedia Company ICMP Flood

This report covers a guided lab from the Google Cybersecurity Certificate. I reviewed the incident scenario and the NIST Cybersecurity Framework (CSF) reference guide, then filled in the incident report analysis template using the five core functions of the NIST CSF.

---

## Summary

A multimedia company experienced a DoS attack that took its network down for two hours until it was resolved. The organization's network services suddenly stopped responding because of a flood of incoming ICMP packets. The incident management team responded by blocking incoming ICMP packets, stopping non-critical network services, and restoring critical network services. An investigation found that the malicious actor sent the ICMP flood into the company's network through a firewall that had not been configured to limit ICMP traffic.

---

## Identify

The attack exploited an unconfigured firewall. Because the firewall did not limit ICMP traffic, the attacker's flood of ICMP packets passed through it and overwhelmed the internal network. The company's hardware, operating systems, and software could not be used normally for the duration of the attack, since normal traffic could not reach any network resources.

The company could not carry out its normal business processes during the outage, including its web design, graphic design, and social media marketing work for clients. The cybersecurity team needs access to the affected systems for immediate remediation.

---

## Protect

The cybersecurity team needs immediate access to the affected network systems during a DoS attack. Administrative privileges should be limited so only the right people have access to firewall and network controls. The cybersecurity team and company leadership both need to be notified so they can work together on the issue, and employees should be made aware of the attack and how it happened.

To prevent this from happening again, the company should:

- Maintain the configuration of its firewalls and review it regularly.
- Use a new firewall rule to limit the rate of incoming ICMP packets.
- Use source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets.
- Use network monitoring software to detect abnormal traffic patterns.
- Use an IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics.

The systems and data that support the company's web design, graphic design, and social media marketing services for small businesses also need to be made more secure.

---

## Detect

The IDS/IPS can alert the security team to unusual activity, such as a spike in incoming ICMP traffic. Network monitoring software should watch for abnormal traffic patterns at all times, and firewall logs should be reviewed for suspicious traffic. A security information and event management (SIEM) tool can collect these logs and alerts in one place, so the team can spot an attack quickly and respond before services go down.

---

## Respond

The incident management team will follow a written DoS response plan. When an ICMP flood is detected, they block incoming ICMP traffic at the firewall, take non-critical network services offline, and restore critical services first so the business can keep running.

As soon as an attack is confirmed, the team alerts IT staff and management. End users are told which services are down, what they cannot access, and when service is expected back. Clients affected by the outage are updated as needed.

To analyze a similar attack, the team reviews firewall and network monitoring logs to find the source IP addresses, checks whether they were spoofed, and works out how the traffic got past the firewall.

To limit the damage, the team isolates or takes affected systems offline and relies on the IDS/IPS and the new ICMP rate limiting rule to filter suspicious traffic.

For improvements, the team will audit firewall settings regularly, run drills on the response plan, and update the plan after every incident based on what they learned.

---

## Recover

To recover from an ICMP flood, the team first stops the attack by blocking the malicious ICMP traffic at the firewall. Critical network services come back online first, then non-critical services once traffic is back to normal. If any systems or data were affected, they are restored from the latest backups and checked to confirm they work properly.

For improvements, the team will keep current backups of firewall and network configurations so services can be restored quickly. They will also document which services count as critical, so the restore order is clear ahead of time, and review the recovery process after every incident to cut downtime.

Throughout recovery, the incident management team keeps IT staff updated on which services are restored and which are still pending. Once normal service returns, end users and management get a notice confirming that all network resources are available again, along with any steps users need to take.

---

## Reflections

This incident shows how one missing firewall rule can make a whole network unavailable. Applying the NIST CSF made it clear that the fix is more than blocking ICMP once. The company needs protective controls, continuous monitoring, and a tested response and recovery plan so the next attack is caught early and causes less downtime.
