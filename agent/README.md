# agent/ README

This directory contains the **agent binary**, the main executable for the Whirlwind metrics collection system. The agent is responsible for:

1. **Collecting Metrics**: Monitors system resources such as CPU, memory, networking, and storage.
2. **Shipping Metrics**: Sends collected metrics to configured endpoints (e.g., Prometheus, HTTP, file-based storage).
3. **Service Management**: Runs as a background service, typically managed through `systemd`.

---

## Files

- `agent_binary`: The compiled Go binary for the Whirlwind agent.

---

## Usage

### Running the Agent
To manually start the agent:
```bash
./agent_binary start
```

### Stopping the Agent
To stop the agent:
```bash
./agent_binary stop
```

---

## Systemd Integration
The agent is designed to run as a `systemd` service. Use the provided `Makefile` to set up the `systemd` service.

### Start the Service
```bash
sudo systemctl start whirlwind
```

### Stop the Service
```bash
sudo systemctl stop whirlwind
```

### Service Status
```bash
sudo systemctl status whirlwind
```

---

## Configuration
The agent uses a configuration file located at:
```
/usr/local/whirlwind/conf.yaml
```
Update this file to configure metrics collection, endpoints, and other settings.