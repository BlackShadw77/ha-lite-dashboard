# HA Lite Dashboard

A lightweight, standalone HTML dashboard for Home Assistant.

Designed to provide a simple interface for monitoring and controlling Home Assistant devices, with support for older browsers and devices, including iOS 12.

Designed with assitance from Claude

**[GitHub Repository](https://github.com/BlackShadw77/ha-lite-dashboard)**

## Features

- Lightweight standalone HTML file
- No additional Home Assistant integrations required
- Compatible with older browsers
- Live Home Assistant entity states
- Device controls for supported entities
- Customisable cards, icons and layouts
- Light and dark themes
- Dashboard layout backup and restore
- GitHub update notifications

## Requirements

- Home Assistant
- Access to the Home Assistant `/config/www/` directory
- A dedicated Home Assistant user account
- A Long-Lived Access Token

## Installation

### 1. Create a Home Assistant user

Create a dedicated Home Assistant user for the dashboard.

1. Navigate to **Settings → People**.
2. Select **Add Person**.
3. Create a user named `Dashboard` (or similar).
4. Ensure the account is a **non-administrator**.

Using a separate account limits the impact of a compromised access token.

### 2. Generate an access token

1. Log in using the new dashboard account.
2. Open your user profile.
3. Navigate to **Security → Long-Lived Access Tokens**.
4. Select **Create Token**.
5. Enter a name, such as `HA Lite Dashboard`.
6. Copy and securely store the generated token.

**Important:** The token is only displayed once. Do not share it or publish it.

### 3. Download the dashboard

Download the latest HTML file from GitHub:

[Download ha-lite-dashboard.html](https://raw.githubusercontent.com/BlackShadw77/ha-lite-dashboard/main/ha-lite-dashboard.html)

### 4. Upload to Home Assistant

Copy the downloaded file into your Home Assistant `www` directory.

`/config/www/ha-lite-dashboard.html`

If the `www` directory doesn't exist, create it.

### 5. Open the dashboard

Access the dashboard using:

`http://HOMEASSISTANT:8123/local/ha-lite-dashboard.html`

Replace `HOMEASSISTANT` with your Home Assistant hostname or IP address.

For example:

`http://homeassistant.local:8123/local/ha-lite-dashboard.html`

On first launch, enter your Home Assistant address and Long-Lived Access Token in the dashboard settings.

If accessing the dashboard directly through Home Assistant, the address can be left blank to use the current connection.

## Updating

Updates are installed manually.

1. Download the latest `ha-lite-dashboard.html` from [GitHub](https://github.com/BlackShadw77/ha-lite-dashboard).
2. Replace the existing file in `/config/www/`.
3. Refresh the dashboard.

Keep the filename unchanged to preserve your existing dashboard URL.

The dashboard can check GitHub for newer versions and notify you when an update is available.

**Note:** Update notifications do not automatically install updates. The *Reload latest version* option reloads the file already hosted on your Home Assistant server.

## Configuration

Dashboard settings and layouts are stored locally in the browser.

Available customisation includes:

- Entity visibility and ordering
- Card names, icons and sizes
- Dashboard themes and colours
- Clock and calendar display
- Entity grouping

### Backup and Restore

Use the **Backup / Restore** option in Edit Mode to export or import dashboard layouts.

This is useful when moving to another device or browser.

## Troubleshooting

| Problem | Suggested fix |
|---|---|
| Connecting indefinitely | Check the Home Assistant address and network connection. |
| Token rejected | Generate a new Long-Lived Access Token. |
| Entities missing | Refresh the dashboard and check entity availability. |
| Old version displayed | Use Reload latest version or clear the browser cache. |
| Layout reset | Restore a previously saved dashboard backup. |

## Security

- Use a dedicated non-administrator account.
- Never publish or share your access token.
- The access token is stored in browser local storage.
- Use HTTPS when accessing Home Assistant remotely.
- Revoke compromised tokens from your Home Assistant profile.

**Remember:** A non-administrator account is recommended, but its API access should still be tested against the devices and actions you intend to use.

## Repository

[BlackShadw77/ha-lite-dashboard](https://github.com/BlackShadw77/ha-lite-dashboard)
