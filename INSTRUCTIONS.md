# 🧩 Installing Ezlo HA Cloud via HACS

This guide shows how to install the **Ezlo HA Cloud** custom integration using [HACS](https://hacs.xyz/), the Home Assistant Community Store.

---

## Prerequisites

- Home Assistant running (any installation type)
- HACS already installed
- Internet connection
- This integration must be on a **public GitHub repo** with the correct structure

---

## 1. Repository Structure

Your repo should be structured like this:

```
home-assistant-ezlo-cloud/
├── custom_components/
│   └── ezlohacloud/
│       ├── __init__.py
│       ├── manifest.json
│       ├── config_flow.py
│       └── ...
├── hacs.json
└── README.md
```

### Sample `hacs.json`

```json
{
  "name": "Ezlo HA Cloud",
  "domain": "ezlohacloud",
  "documentation": "https://github.com/yourname/home-assistant-ezlo-cloud",
  "issue_tracker": "https://github.com/yourname/home-assistant-ezlo-cloud/issues",
  "codeowners": ["@yourname"],
  "requirements": [],
  "version": "1.0.0"
}
```

---

## 2. Add Custom Repository in HACS

1. Open Home Assistant → **HACS** → **Integrations**
2. Click the **3-dot menu** (top-right) → **Custom repositories**
3. Add:
   - **URL**: `https://github.com/yourname/home-assistant-ezlo-cloud`
   - **Category**: `Integration`
4. Press **Add**

---

## 3. Install the Integration

1. HACS will now show `Ezlo HA Cloud` in the Integrations tab
2. Click on it → Press **Install**
3. **Restart Home Assistant**

---

## 4. Set Up in Home Assistant

1. Go to **Settings → Devices & Services**
2. Click **+ Add Integration**
3. Search for **Ezlo HA Cloud**
4. Follow the configuration flow

---

## Updating the Integration

- When you tag new releases on GitHub, HACS will notify users to update.
- Keep the version updated in `hacs.json` and GitHub releases.

---

## Troubleshooting

- Make sure your repository is public
- Folder name **must match** the `domain` in `manifest.json` and `hacs.json`
- Restart HA after installation
- Check **Developer Tools → Logs** for any errors

---