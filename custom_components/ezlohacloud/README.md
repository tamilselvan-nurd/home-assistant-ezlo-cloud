# Install Steps

1. Uzip / clone the plugin repo under the components folder under home assistant.
2. Add the following snippet in configuration file under core/config/configuration.yaml with the following,

```toml
http:
  use_x_forwarded_for: true
  trusted_proxies:
    - 127.0.0.1 # localhost
    - ::1 # localhost for IPv6
    - 137.184.147.158 # Your DigitalOcean server's public IP or ezlo domain/ip for frp server.
    - 172.17.0.1 # The proxy IP reported in the error
```
3. Add the following entry under homeassistant/generated/integrations.json
```json
"ezlohacloud": {
  "name": "Ezlo HA Cloud",
  "integration_type": "hub",
  "config_flow": true,
  "iot_class": "cloud_polling"
}
```

-------

# Error Solutions
# Error : not_implemented when adding integration

This means that the integration config flow is set to true in manifest which triggers ha to look for it. Make it false.


### Note: Once you have updated your manifest and created the config_flow.py, you will need to run `python3 -m script.hassfest` (one time only) for Home Assistant to activate the config entry for your integration.

# Ezlo Cloud – Home Assistant Custom Integration

This repository contains a custom Home Assistant integration for Ezlo Cloud devices.

---

## Development Setup (VS Code + Home Assistant Core Devcontainer)

If you're using the official Home Assistant Core development environment via VS Code devcontainers, follow these steps to mount and test this integration live.

---

### 1. Prerequisites

- You’ve cloned [`home-assistant/core`](https://github.com/home-assistant/core) locally
- You have VS Code + the **Dev Containers** extension installed
- You have **this repo cloned** locally (e.g., `home-assistant-ezlo-cloud`)

---

### 2. Update `devcontainer.json` in HA Core

In your `home-assistant/core/.devcontainer/devcontainer.json`, add this to the `"mounts"` section:

```json
"mounts": [
  "source=/absolute/path/to/home-assistant-ezlo-cloud/custom_components/ezlohacloud,target=${containerWorkspaceFolder}/config/custom_components/ezlohacloud,type=bind"
]
```

Replace /absolute/path/to/... with the actual path on your machine.

---

### 3. Rebuild the Dev Container
In VS Code (from HA Core project):

```Press Cmd+Shift+P```

Choose: Dev Containers: Rebuild and Reopen in Container

### 4. Start Home Assistant

### 5. Confirm It’s Loaded
Open the UI at http://localhost:8123, go to:

```Developer Tools → Logs```
