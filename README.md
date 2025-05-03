# Intune Device Diagnostic Tool
<img src="https://github.com/user-attachments/assets/de94eba5-c736-4b6e-9142-08a00d769454" alt="Imagen" width="300" height="300">

This PowerShell script allows diagnostics and searches on devices registered in Microsoft Intune, filtering by various conditions and displaying relevant information. It also provides troubleshooting assistance to help identify potential issues with Intune devices, such as inactivity or licensing problems.

## Features

- **Device Search**: Search for a device by name in Intune and Microsoft Defender.
- **Device Information**: Retrieves and displays detailed information about the device, including OS version, enrollment type, last activity, and more.
- **Troubleshooting**: 
  - Identifies devices that are non-compliant with Intune policies.
  - Checks if the device is inactive based on its last sync date.
  - Compares the device's OS version with the latest available version.
  - Verifies the device's compliance state and ownership.
- **License Check**: Verifies if the device's assigned owner has the necessary Intune licenses.

## Requirements

- **PowerShell**: This script is designed to run in PowerShell.
- **Microsoft Graph PowerShell Module**: The script uses the Microsoft Graph module to interact with Intune and retrieve device data.
- **Internet Access**: Required to fetch the latest release information for Windows updates and to interact with Microsoft Graph.

## Prerequisites

1. Install the Microsoft Graph PowerShell module (if not already installed):

   ```powershell
   Install-Module -Name Microsoft.Graph -Scope CurrentUser -Force

## Permissions

Make sure you have appropriate permissions to access the Intune devices and Microsoft Graph API. You must have the following permissions:

- `DeviceManagementManagedDevices.Read.All`
- `DeviceManagementConfiguration.Read.All`

## Usage

1. Clone or download this executable to your local machine.
2. Run the executable in PowerShell.
3. Enter the device name you wish to search for in Intune.
4. The script will display detailed information about the device, including:
   - Device name, ID, enrollment type, and registration information.
   - Compliance state and last sync time.
   - A troubleshooting report that identifies any issues with the device's compliance, version, or activity.
5. The script will also check if the device's owner has the required Intune licenses.

## How It Works

- **Device Search**: The script allows you to input a device name, and it searches for the device across different Intune management types (e.g., Intune).
- **Device Information**: Once a device is found, it retrieves information such as OS version, registration date, last activity, and enrollment profile.
- **Compliance State**: The script checks the device’s compliance state, identifying whether it’s compliant, non-compliant due to inactivity, or non-compliant for other reasons.
- **Troubleshooting**:
   - It compares the device's OS version to the latest available version and flags if an update is needed.
   - It checks the device's last sync date to identify inactivity.
   - It verifies if the device has a valid owner assigned and if that owner has the required licenses.

## Troubleshooting

- If the device is not found, ensure the device name is correct and exists in Intune or Microsoft Defender.
- If there are issues connecting to Microsoft Graph, ensure you have the necessary permissions and are connected to the correct tenant.
- If the script is unable to check for the latest OS version, it may be due to an issue with the release page URL or the OS version format.

<img src="https://github.com/user-attachments/assets/69b04ebd-1159-4e7a-a84c-9c2a5ec69bd4" alt="Imagen" width="600" height="800">
