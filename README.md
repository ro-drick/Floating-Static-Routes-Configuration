# Packet Tracer Lab: Floating Static Routes

## Lab Overview

This lab explores the use of **dynamic routing protocols** and **floating static routes** within an enterprise network. It demonstrates how to configure static routes that act as backups when primary links fail, ensuring network connectivity between key devices like **PC1** and **SRV1**.

## Lab Instructions

### 1. Checking Routing Protocols and Routes

#### Tasks:
- **Check the routing tables** of both **R1** and **R2**.
- Identify the **dynamic routing protocol** being used in **Enterprise A**.
- Determine which route is selected when **PC1** attempts to:
  - Access **SRV1**.
  - Access the **remote server** at IP `1.1.1.1` over the Internet.
- **Test connectivity** by pinging **SRV1** and the remote server (`1.1.1.1`).

#### Expected Results:
- You'll identify the dynamic routing protocol and the correct route for accessing **SRV1** and the remote server.
- Successful **pings** indicate correct routing.

### 2. Configuring Floating Static Routes

#### Tasks:
- **Configure floating static routes** on **R1** and **R2** to allow **PC1** to reach **SRV1** in case the link between **R1** and **R2** fails.
- **Verify** if the newly configured routes are added to the routing tables of both routers.

#### Expected Results:
- The floating static routes should not be visible in the routing table immediately, as they act as backup routes.

### 3. Simulating Link Failure

#### Tasks:
- **Shut down** the interface **G0/2/0** on either **R1** or **R2**.
- Observe if the floating static routes are now **added to the routing tables** of both routers.
- **Ping** from **PC1** to **SRV1** to confirm network connectivity.

#### Expected Results:
- The floating static routes should enter the routing table after the link failure.
- **PC1** should successfully ping **SRV1**, indicating that the backup route is functioning correctly.

---

## Configuration Notes

- The lab demonstrates how floating static routes provide **redundancy** in the event of a link failure.
- Proper configuration ensures that the network remains operational even if the primary route fails.

---

## How to Use the Lab

1. **Open the Packet Tracer file** (`Floating Static Routes Solved.pkt`).
2. **Follow the steps** outlined above to observe and configure routing protocols.
3. Experiment by **shutting down interfaces** and testing network connectivity.
4. **Modify the configurations** as needed to understand the behavior of floating static routes.

---
