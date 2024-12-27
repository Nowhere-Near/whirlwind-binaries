# installer/ README

This directory contains the **installer binary**, which prepares the environment for the Whirlwind agent.

---

## Files

- `install`: The compiled Go binary for the Whirlwind installer.

---

## Purpose
The installer:
1. Sets up necessary directories (e.g., `/usr/local/whirlwind/`).
2. Copies the default configuration file.
3. Creates log files and prepares the environment for the agent to run.

---

## Usage
To run the installer:
```bash
sudo ./install
```

This will:
- Create the necessary directories.
- Copy the configuration file to `/usr/local/whirlwind/conf.yaml`.
- Set up logs in `/usr/local/whirlwind/logs/`.

---

## Requirements
- Ensure the installer binary (`install`) has execution permissions:
  ```bash
  chmod +x install
  ```
- Run the installer with root privileges to create directories and set up files.

---

## Post-Installation
After running the installer, you can start the Whirlwind agent using the `systemd` service created during installation. Refer to the `agent/README.md` for details.
