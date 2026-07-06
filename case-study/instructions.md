**What a case study is in this context:**

A printed document, usually 1-3 pages, that tells the full story of a project with depth that doesn't fit on a resume. Problem statement, design decisions and why you made them, implementation, what you attacked, what was detected, what wasn't, and what you'd do differently. It proves to the interviewer that you actually understand what you built rather than just following a tutorial.

**For your Wazuh lab specifically, structure it like this:**

**Objective** - Why you built it, what threat scenarios you wanted to simulate.

**Architecture and Design Decisions** - The dual-pfSense topology, why two routers instead of one, why you isolated the attacker LAN from SIEM visibility, how the OPT1 point-to-point link works and why you used static addressing there instead of DHCP.

**Attack Scenarios and Detection Results** - Three sections: SSH brute force via Hydra (what you ran, what Wazuh caught, what the active response did), privilege escalation via sudo (how you triggered it, what rule fired), and FIM on Windows (what you configured, what events were generated).

**What Failed or Was Dropped and Why** - The agent-000 syslog limitation that killed pfSense/Suricata as a log source, the Wazuh-on-Debian failure, the Ubuntu LVM disk issue. This section is what separates someone who actually did the lab from someone who just wrote about doing it.

**Future Improvements** - IDS/IPS integration, the pfSense/Suricata problem you'd solve differently.

The failures section is your strongest differentiator. Most candidates only document what worked.
