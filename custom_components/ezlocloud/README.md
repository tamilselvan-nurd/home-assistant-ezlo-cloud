# Error Solutions
# Error : not_implemented when adding integration

This means that the integration config flow is set to true in manifest which triggers ha to look for it. Make it false.


### Note: Once you have updated your manifest and created the config_flow.py, you will need to run `python3 -m script.hassfest` (one time only) for Home Assistant to activate the config entry for your integration.