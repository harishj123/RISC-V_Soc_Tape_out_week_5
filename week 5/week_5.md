
---

# 🧠 Week 5 — VSD Hardware Design Program

## 🚀 OpenROAD Installation & Flow Guide

### 👋 Welcome to Week 5!

Welcome to **Week 5** of the **VSD Hardware Design Program**!
This week, we dive into **OpenROAD** — an open-source, fully automated **RTL-to-GDSII** flow for **digital integrated circuit (IC) design**.

OpenROAD enables a complete end-to-end IC design flow, supporting:

* 🧩 Synthesis
* 🏗️ Floorplanning
* 🧱 Placement
* ⏰ Clock Tree Synthesis (CTS)
* 🛣️ Routing
* 🖼️ Final Layout Generation (GDSII)

It’s widely used for **academic research** and **industry prototyping**, allowing **rapid design iterations** and full design automation.

---

## 📚 Contents

1. [Steps to Install OpenROAD and Run GUI](#steps-to-install-openroad-and-run-gui)
2. [ORFS Directory Structure and File Formats](#orfs-directory-structure-and-file-formats)

---

## ⚙️ Steps to Install OpenROAD and Run GUI

### 🧩 1. Clone the OpenROAD Repository

```bash
git clone --recursive https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts
cd OpenROAD-flow-scripts
```

---

### 🔧 2. Run the Setup Script

This installs all dependencies and prepares the environment.

```bash
sudo ./setup.sh
```

---

### 🏗️ 3. Build OpenROAD

Build the OpenROAD tool locally:

```bash
./build_openroad.sh --local
```

---

### ✅ 4. Verify Installation

Activate the environment and verify tools:

```bash
source ./env.sh
yosys -help
openroad -help
```

If both commands respond with help menus, your installation is successful!

---

### 🧠 5. Run the OpenROAD Flow

Run a full **RTL-to-GDSII** flow using:

```bash
cd flow
make
```

This will automatically execute synthesis, floorplanning, placement, CTS, and routing steps.

---

### 🖥️ 6. Launch the GUI

Visualize your final chip layout in the OpenROAD GUI:

```bash
make gui_final
```

🎉 **Installation Complete!**
You can now explore and experiment with the **full RTL-to-GDSII flow** using **OpenROAD**.

---

## 🗂️ ORFS Directory Structure and File Formats

```
OpenROAD-flow-scripts/
├── docker/         -> Docker-based installation and run scripts
├── docs/           -> Documentation for OpenROAD and flow scripts
├── flow/           -> Files related to running RTL-to-GDS flow
├── jenkins/        -> Regression tests for each build update
├── tools/          -> Required tools for RTL-to-GDS flow
├── etc/            -> Dependency installer and configuration scripts
├── setup_env.sh    -> Environment setup script for the flow
```

### Inside the `flow/` Directory

```
flow/
├── design/         -> Built-in RTL-to-GDS example designs across technology nodes
├── makefile        -> Automation script to run the entire flow
├── platform/       -> Contains PDK libraries, LEF, GDS, and technology files
├── tutorials/      -> Learning resources and example flows
├── util/           -> Utility scripts and helpers
├── scripts/        -> Main scripts that control flow stages
```

---

## 🌟 Summary

You’ve successfully:

* Installed and configured **OpenROAD**
* Learned the full flow from **RTL to GDSII**
* Explored the **directory structure** and how the tools connect

💡 Now you’re ready to dive deeper into IC design automation with OpenROAD!

---
