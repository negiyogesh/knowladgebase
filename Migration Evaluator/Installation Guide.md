**Prerequisite**
1. Has an account been created on https://console.tsologic.com?
2. Windows Server Created (2016+)
3. Connectivity to VMware vCenter -- 443 Port and read only user.
4. Simple Network Management Protocol (SNMP) (port 161).
5. Connectivity via WMI (Windows Management Instrumentation) (Network connectivity via TCP port 135 + ephemeral TCP port range (49152 - 65535)) 


===========
**Data Synchronization with AWS**

Steps:
1. Install the Migration Evaluator Bootstrapper
2. Download and save the collector specific encryption certificate from https://console.tsologic.com/discover/collectors onto the new designated server.
3. Install the Migration Evaluator Collector.
\>>>>

4. Configure Collection from VMware
5. Configure Operating System Credentials


-------------------
    Access Migration Evaluator: Log in to the Migration Evaluator interface.

**Configure OS Credential:** You'll need to provide credentials for accessing the Windows Management Instrumentation (WMI) on each virtual machine.

    a. Go to the Migration Evaluator interface.

    b. Find the section where you can add OS credentials. This might be labeled as "Credentials", "OS Credentials", or something similar.

    c. Add the appropriate credentials for accessing WMI on each VM. You'll need administrative credentials (e.g., username and password) for each VM.

    d. Ensure that the credentials you provide have sufficient permissions to access WMI on the target VMs.

    Adding Multiple Credentials: Since you have 60 VMs, you'll need to add credentials for each VM individually unless they share the same administrative credentials. If they share the same credentials, you only need to add them once.

    Test Credentials: After adding the credentials, it's a good practice to test them to ensure they work properly. This can usually be done within the Migration Evaluator interface.

    Assess OS Level Metrics: Once the credentials are added and tested successfully, you can proceed with assessing OS level metrics using Migration Evaluator. It will use the provided credentials to gather necessary information from each VM via WMI.

    Review Results: After the assessment, review the results provided by Migration Evaluator regarding the OS level metrics of your VMs.