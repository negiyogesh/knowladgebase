**Connectivity via WMI**
1. • Network connectivity via ICMP
2. Network connectivity via TCP port 135 + ephemeral TCP port range (49152 - 65535)
3. User Should have following rights:
    > Local Administrator Rights.
    > Remote Access Permissions.
    > WMI Namespace Permissions.
    > Firewall Settings: Make sure that the Windows Firewall or any other firewall software on the VMs allows incoming WMI requests. By default, WMI uses DCOM communications, which might require additional firewall configuration.
