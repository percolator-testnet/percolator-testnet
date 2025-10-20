# Percolator Testnet

**Percolator** is a **sharded perpetual exchange protocol** built on **Solana**, designed for high-performance decentralized trading.
This public **testnet** invites participants to run local nodes, monitor performance, and help identify bugs before mainnet deployment.

---

## 🚀 How to Join the Testnet

### 1. Install the Node

Download the latest **Percolator Node** build for your OS:

> 🔗 [Download Node (.exe)](../../releases)

Requirements:

* **Windows 10+ / Linux / macOS**
* **Solana CLI** (v2.0 or higher)
* **Rust toolchain** (optional, for developers)

`After downloading, extract the archive`

---

### 2. Start the Local Node

Run the node:`percolator-node.exe`

The node will automatically:

* Connect to the Solana test validator
* Initialize Router & Slab programs
* Start processing local trades and routing activity

---

### 3. Monitor Logs and Errors

All operational logs are written to the `logs/` directory:

```
logs/percolator-router.log  
logs/percolator-slab.log  
```

You can also view live output in the terminal:

```bash
percolator-node.exe --mode testnet --verbose
```

If you notice crashes, inconsistent calculations, or PDA derivation errors — collect the log file and share it in the issue tracker.

---

### 4. Testnet Objectives

* Validate **node stability** (Router / Slab subsystems) under continuous uptime
* Detect memory leaks and allocation overflows
* Verify PDA derivations and cross-slab margin logic
* Stress-test matching and liquidation modules
* Report bugs via GitHub or Discord

Active testers contributing useful logs or bug reports will be **eligible for future rewards and airdrops**.

---

## ⚙️ Core Programs

| Program    | Purpose                                     | Program ID                                    |
| ---------- | ------------------------------------------- | --------------------------------------------- |
| **Router** | Collateral management, cross-margin routing | `RoutR1VdCpHqj89WEMJhb6TkGT9cPfr1rVjhM3e2YQr` |
| **Slab**   | Matching engine and trade settlement        | `SLabZ6PsDLh2X6HzEoqxFDMqCVcJXDKCNEYuPzUvGPk` |

---

## 🧩 Debugging & Testing

To verify local functionality, run basic self-tests:

```bash
percolator-node.exe --test
```

Integration with **Surfpool** (optional):

```bash
git clone https://github.com/txtx/surfpool
cd surfpool && npm install && npm run validator
```

Then connect your Percolator node to Surfpool for live state testing.

---

## 📬 Feedback

If your node crashes, hangs, or fails to process instructions:

1. Attach your log files (`logs/*.log`)
2. Include OS version and node build number
3. Submit the report via GitHub Issues or the testnet feedback form

---

**Status:** Testnet is **live and active** 🟢
Run your node, contribute data, and help stabilize the Percolator network.

**Last Updated:** October 2025
