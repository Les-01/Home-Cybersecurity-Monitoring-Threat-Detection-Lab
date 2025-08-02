# Home-Cybersecurity-Monitoring-Threat-Detection-Lab
Home Cybersecurity Monitoring & Threat Detection Lab

Self-Initiated Project
Overview

This self-directed project involved the design and deployment of a fully virtualised Security Operations Centre (SOC) lab simulating a small enterprise network. The lab was built to monitor and investigate both simulated and real-world cyberattacks using open-source and enterprise-grade SIEM tools. The project showcases practical experience in blue team operations, from configuring network infrastructure to detecting and responding to threats using Splunk, Security Onion, Suricata, and Kibana.
Objectives

    Build a virtual lab environment simulating an enterprise network

    Deploy and configure SIEM platforms (Splunk and Security Onion)

    Simulate a variety of cyberattacks (e.g. scanning, brute-force, lateral movement)

    Detect and investigate threats using Suricata, Kibana, and Splunk

    Respond to and mitigate both simulated and real-world incidents

Lab Setup

    Installed VMware Workstation Pro to host all virtual machines

    Deployed and configured:

        PfSense Firewall: configured rules and interfaces to simulate enterprise topology

        Windows 11 Pro VM: user workstation, later joined to domain

        Windows Server 2019: Active Directory, DNS Server, intentionally misconfigured for exploitation

        Ubuntu Server: Splunk Enterprise SIEM with Universal Forwarder on Windows Server

        Security Onion: full-stack SOC platform with Suricata and Kibana

        Kali Linux: attacker machine

        Metasploitable 2: intentionally vulnerable target

    Configured AD users/groups and DNS

    Enabled log forwarding to both Splunk and Security Onion for cross-analysis

Simulated Attacks

    Reconnaissance:

        Ping sweeps from Kali Linux

        Nmap scans to enumerate open ports and services

    Password Attacks:

        Brute-force login attempts targeting Windows Server using Hydra

    Real-World Incident:

        Detected an unauthorised external IP performing exploitation attempts on vulnerable hosts

Threat Detection & Response

    Security Onion (with Suricata and Kibana) and Splunk successfully detected:

        Ping sweeps

        Nmap scans

        Failed login attempts

        Suspicious traffic from external IP addresses

    Confirmed breach using Suricata logs and Kibana dashboards

    Responded by:

        Identifying and isolating compromised systems

        Revoking privileges

        Locking down firewall rules via PfSense

        Restoring network to a secure state while maintaining analyst access through Windows 11 VM

Tools & Technologies

    SIEMs: Splunk Enterprise, Security Onion

    IDS/IPS: Suricata

    Firewall: PfSense

    Monitoring & Visualisation: Kibana, Splunk dashboards

    Attack Simulation: Kali Linux, Hydra, Nmap

    Operating Systems: Windows Server 2019, Windows 11 Pro, Ubuntu, Kali Linux

    Virtualisation: VMware Workstation Pro

Key Outcomes

    Demonstrated full threat lifecycle coverage: detection, investigation, and response

    Validated effectiveness of SIEM tools in identifying real-time attacks

    Gained hands-on experience with blue team workflows and security architecture

    Handled a real-world intrusion attempt and executed a full incident response

This project was developed independently to enhance practical cybersecurity skills and demonstrate end-to-end threat monitoring and incident response capabilities in a controlled lab environment.
