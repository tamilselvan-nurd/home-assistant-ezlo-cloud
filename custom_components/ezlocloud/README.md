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