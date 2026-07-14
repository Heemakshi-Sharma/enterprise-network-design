This document summarizes some of the common issues encountered during the implementation of the Enterprise Network Design project and the steps taken to resolve them.

## Issue 1: Devices in Different VLANs Could Not Communicate - Hosts connected to different VLANs were unable to communicate.
Root Cause : Inter-VLAN Routing was not configured correctly.
Solution
- Verified VLAN assignments.
- Configured Router-on-a-Stick.
- Configured subinterfaces with the correct VLAN encapsulation.
- Assigned the correct default gateway to end devices.
Verification : Devices in different VLANs successfully communicated after the configuration was corrected.

## Issue 2: OSPF Neighbors Were Not Forming - Routers were not establishing OSPF neighbor relationships.
Root Cause : Incorrect OSPF configuration and missing network advertisements.
Solution
- Verified router interfaces.
- Confirmed Area IDs.
- Added the required network statements.
- Verified interface status.
Verification : OSPF neighbors formed successfully and routes were exchanged.

## Issue 3: Routing Between Branch Offices Failed - Traffic between branch offices could not reach the destination network.
Root Cause : Routing information was incomplete.
Solution
- Verified routing tables.
- Corrected OSPF advertisements.
- Confirmed interface IP addressing.
Verification : Successful end-to-end connectivity between all branch offices.

## Issue 4: VLAN Configuration Errors : Hosts connected to the same switch could not communicate as expected.
Root Cause : Incorrect VLAN assignment
Solution
- Verified VLAN database.
- Assigned ports to the correct VLAN.
- Confirmed switchport mode.
Verification : Communication within each VLAN was restored.

## Issue 5: Trunk Link Misconfiguration : VLAN traffic was not passing between switches.
Root Cause : Incorrect trunk configuration.
Solution
- Configured trunk ports.
- Verified allowed VLANs.
- Checked encapsulation settings.
Verification : Traffic between switches flowed successfully across trunk links.

During this project, Cisco IOS verification commands such as:

- show ip route
- show ip ospf neighbor
- show vlan brief
- show interfaces trunk
- show running-config

were used extensively to isolate and resolve network issues.

The troubleshooting process followed a systematic approach of identifying the problem, verifying the configuration, implementing corrective actions, and validating the solution.
