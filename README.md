# Ezlo HA Cloud

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)
[![GitHub release](https://img.shields.io/github/release/tskezlo/home-assistant-ezlo-cloud.svg)](https://github.com/tskezlo/home-assistant-ezlo-cloud/releases)
[![GitHub stars](https://img.shields.io/github/stars/tskezlo/home-assistant-ezlo-cloud.svg)](https://github.com/tskezlo/home-assistant-ezlo-cloud/stargazers)

A Home Assistant integration for Ezlo Cloud connectivity.

## Installation

### Option 1: HACS (Recommended)

1. Make sure you have [HACS](https://hacs.xyz/) installed
2. Add this repository as a custom repository in HACS
3. Install "Ezlo HA Cloud" from the integrations tab

### Option 2: Manual Installation

1. Download the latest release from the [releases page](https://github.com/tskezlo/home-assistant-ezlo-cloud/releases)
2. Extract the `ezlocloud` folder to your `custom_components` directory
3. Restart Home Assistant

### Option 3: Direct Install Button

[![Open your Home Assistant instance and show the add integration dialog with a specific repository set up.](https://my.home-assistant.io/badges/config_flow_start.svg)](https://my.home-assistant.io/redirect/config_flow_start/?domain=ezlohacloud)

Click the button above to open Home Assistant and add this integration directly.

## Configuration

After installation, you can configure the integration through the Home Assistant UI:

1. Go to **Settings** → **Devices & Services**
2. Click **Add Integration**
3. Search for "Ezlo HA Cloud"
4. Follow the configuration flow

## Requirements

- Home Assistant 2023.1.0 or later
- Python packages: `requests`, `tomli`, `tomlkit`, `aiohttp`

## Features

- Cloud polling integration
- Config flow support
- HomeKit compatibility

## Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/tskezlo/home-assistant-ezlo-cloud/issues) page
2. Create a new issue if your problem isn't already reported
3. Provide as much detail as possible about your setup and the issue

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Home Assistant community
- Ezlo team for providing the cloud API
