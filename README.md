# Linux Fundamentals: System Information and Network Connectivity

This project explores fundamental Linux commands using a Kali Linux virtual machine to inspect system information, hardware resources, storage capacity, uptime, and network connectivity. It demonstrates practical command-line skills for Linux system administration and cybersecurity fundamentals.

## Table of Contents

- Project Overview
- Network Topology
- Tools and Technologies
- Configuration Steps
- Results and Findings
- Author

## Project Overview

The purpose of this project is to develop practical knowledge of Linux fundamentals by executing basic system administration and networking commands in a Kali Linux virtual machine.

The main objectives are to:

- Identify the current Linux username, hostname, and working directory.
- Retrieve operating system and kernel information.
- Inspect CPU specifications and available memory.
- Check available disk space and system uptime.
- Test network connectivity using the `ping` command.
- Compare round-trip times when pinging different IP addresses.

## Network Topology

The project uses a **Kali Linux virtual machine** to perform system information checks and basic network connectivity tests against external IP addresses.

### Network Layout

```
+----------------------------------+
|       Host Computer              |
|                                  |
|  +----------------------------+  |
|  | Kali Linux Virtual Machine |  |
|  |                            |  |
|  | Username: kali             |  |
|  | Hostname: Kali             |  |
|  | Directory: /home/kali      |  |
|  +-------------+--------------+  |
|                |                 |
+----------------|-----------------+
                 |
          Network / Internet
                 |
          +------+------+
          |             |
     Google IP      Google DNS
  172.217.22.78      8.8.8.8
```

### System and Network Details

- **Virtual machine username:** `kali`
- **Hostname:** `Kali`
- **Current working directory:** `/home/kali`
- **Operating system:** Kali Linux
- **Kernel version:** `6.19.14`, as reported in the assignment.
- **Total RAM:** `1.9 GiB`
- **Available disk space on the main partition:** `59 GiB`
- **External IP address tested:** `172.217.22.78`
- **Additional connectivity test target:** `8.8.8.8`


## Tools and Technologies

- **Kali Linux:** Linux distribution used for the practical exercises.
- **Linux command-line terminal:** Interface for executing system administration and networking commands.
- **Virtual machine:** Environment in which Kali Linux was running.
- **`whoami`:** Identifies the current logged-in user.
- **`hostname`:** Displays the system hostname.
- **`pwd`:** Displays the current working directory.
- **`uname -a`:** Retrieves kernel and system information.
- **`lscpu`:** Displays CPU architecture and processor details.
- **`free -h`:** Reports memory usage in human-readable units.
- **`df -h`:** Displays filesystem disk space usage.
- **`uptime`:** Reports system uptime and related load and user information.
- **`ping`:** Tests network reachability and measures round-trip time.

## Configuration Steps

### 1. Identify the Current User

Execute the following command in the Kali Linux terminal:

```
whoami
```

The command identifies the current user. The result recorded in the assignment was `kali`.

### 2. Check the Hostname

Run:

```
hostname
```

The command displays the virtual machine's hostname, reported as `Kali`.

### 3. Identify the Current Working Directory

Execute:

```
pwd
```

The output identifies the current directory as `/home/kali`.

### 4. Retrieve Operating System and Kernel Information

Run:

```
uname -a
```

This command displays detailed kernel and system information. The assignment reports the kernel version as `6.19.14`.

### 5. Inspect CPU Information

Execute:

```
lscpu
```

The command displays CPU-related details, including processor architecture and other available processor specifications. The assignment does not provide the individual CPU values in its text.

### 6. Check Memory Usage

Run:

```
free -h
```

This command reports total, used, and available memory in a human-readable format. The virtual machine's total RAM was reported as `1.9 GiB`.

### 7. Check Disk Space

Execute:

```
df -h
```

The command displays filesystem capacity, used space, available space, and mount points. The assignment reports `59 GiB` of available disk space on the main partition.

### 8. Check System Uptime

Run:

```
uptime
```

This command displays how long the system has been running, along with information such as the number of logged-in users and system load averages.

### 9. Test Network Connectivity

Use the following command to send four ping requests to Google's public DNS server:

```
ping -c 4 8.8.8.8
```

The `-c 4` option limits the test to **four ICMP echo requests**. The assignment reports an average round-trip time of `92.373 ms` and no packet loss for this test.

### 10. Test Connectivity to Google's IP Address

Run:

```
ping -c 4 172.217.22.78
```

This command tests connectivity to the IP address recorded for Google in the assignment.

The assignment reports an average round-trip time of `18.196 ms` for `172.217.22.78`, compared with `92.373 ms` for `8.8.8.8`.

## Results and Findings

The project successfully documented several aspects of the Kali Linux environment and demonstrated the use of basic Linux system administration and networking commands.

### System Information Results

| Parameter                                  | Result       |
| ------------------------------------------ | ------------ |
| Username                                   | `kali`       |
| Hostname                                   | `Kali`       |
| Working directory                          | `/home/kali` |
| Kernel version                             | `6.19.14`    |
| Total RAM                                  | `1.9 GiB`    |
| Available disk space on the main partition | `59 GiB`     |

### Network Connectivity Results

| Test parameter                              | Result          |
| ------------------------------------------- | --------------- |
| IP address tested                           | `8.8.8.8`       |
| Average round-trip time for `8.8.8.8`       | `92.373 ms`     |
| Packet loss for the reported test           | `0%`            |
| Google IP address recorded                  | `172.217.22.78` |
| Average round-trip time for `172.217.22.78` | `18.196 ms`     |

### Key Findings

- **System identification:** The `whoami`, `hostname`, and `pwd` commands provided the username, hostname, and current directory.
- **Hardware and resource monitoring:** The `lscpu`, `free -h`, and `df -h` commands demonstrated how to inspect processor details, memory, and storage.
- **System monitoring:** The `uptime` command provided information about the running state of the virtual machine.
- **Network connectivity:** The ping test to `8.8.8.8` reported no packet loss, indicating that all four requests were received successfully during the recorded test.
- **Round-trip time comparison:** The recorded average response time for `172.217.22.78` was lower than that for `8.8.8.8`. Differences may result from routing, network conditions, server location, and response handling. The measurements alone do not establish network congestion as the cause.

Overall, the project provided practical experience with essential Linux commands and basic network troubleshooting techniques relevant to system administration and cybersecurity.

## Author

- **Name:** Osawaru Usunobun
- **GitHub:** [Add your GitHub profile URL here](https://github.com/usunben-cyber/).
- **Contact:** usunben@yahoo.com
