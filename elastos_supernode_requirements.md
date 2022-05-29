# Requirements

A new Linux operation system is required to run Elastos Supernode.

- **User**
  - should feel **comfortable with Linux** or similar **POSIX shell environment**
  - has access to the **cloud computing**: [Amazon EC2](https://aws.amazon.com/ec2/), [Microsoft Azure VM](https://azure.microsoft.com/en-us/services/virtual-machines/), [Google Cloud Compute Engine](https://cloud.google.com/compute/)
  - Or has permission to place a server in your **home** or **office** if the room or building has free space, cheap electric supply, and good noise insulation.
- **Public Network**
  - **TCP/IP** the current Internet is required to bootstrap the new one
  - Use the **non-metered connection** to prevent a high usage billing.
- **Server Hardware**
  - **CPU**: **2 cores** or more
  - **RAM**: **32 GB** or more
  - **HDD**: **200 GB** or more
    - A solid-state drive (SSD) is a plus but not a must. A hard drive (HDD) should be OK.
- **Server Software**
  - **OS**: **Ubuntu 20.04 LTS** 64 Bit or newer
    - Use **Ubuntu** because the developer uses macOS and Ubuntu to do the test harness. But it is your freedom of choice of other distributions.
    - **LTS** is better because LTS has a longer product life than the **non-LTS** version. (See [Ubuntu Releases](https://wiki.ubuntu.com/Releases))
    - The script prefers a **freshly installed** OS because it reduces conflicts with the old setup. It is time-consuming to debug such conflicts and do the related support work.
- **Server Security Rules**
  - The following ports need to be accessible from anywhere (0.0.0.0/0). For a cloud server, please modify the inbound rules.

| Program | Protocol and Port Range | Purpose           |
| ------- | ----------------------- | ----------------- |
| ELA     | TCP 20338               | ELA P2P           |
| ELA     | TCP 20339               | ELA DPoS          |
| DID     | TCP 20608               | DID P2P           |
| ESC     | TCP+UDP 20638           | ESC P2P           |
| ESC     | TCP 20639               | ESC DPoS          |
| EID     | TCP+UDP 20648           | EID P2P           |
| EID     | TCP 20649               | EID DPoS          |
| Arbiter | TCP 20538               | Arbiter P2P       |
| Carrier | UDP 3478                | Carrier P2P       |
| Carrier | TCP 33445               | Carrier TCP Relay |
| Carrier | UDP 33445               | Carrier P2P       |