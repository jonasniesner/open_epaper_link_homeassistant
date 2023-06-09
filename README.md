# OpenEPaperLink integration for Home Assistant

Home Assistant Integration for the <a href="https://github.com/jjwbruijn/OpenEPaperLink">OpenEPaperLink</a> project

Feature Request and code contributions are welcome!

## Functionality

### Sensors

Every sensor of the tags is exposed in Home Assistant.
Every tag and the AP is exposed as a device.

### Services

At the moment 3 services are exposed:

#### Download Image

Download an image from the provided url and if required, resized it for the esl it should be displayed on.

This requires that the esl has checked in once before fo Home Assistant knows the hardware type of it so if this service fail, wait 10 to 20 minutes.

#### 5 Line Display

Displays 5 (or up to 10) lines of text on a small 1.54" esl. If a text line contains a newline, it will be split in 2 lines.

#### 4 Line Display

Displays 4 (or up to 8) lines of text on a 2.9" esl. If a text line contains a newline, it will be split in 2 lines.

## Installation

### If you use [HACS](https://hacs.xyz/):

1. Click on HACS in the Home Assistant menu
2. Click on the 3 dots in the top right corner
3. Select "Custom repositories"
4. Add the URL to the repository
5. Select the Integration category
6. Click the "ADD" button

7. Click on HACS in the Home Assistant menu
8. Click on `Integrations`
9. Click the `EXPLORE & DOWNLOAD REPOSITORIES` button
10. Search for `OpenEPaperLink`
11. Click the `DOWNLOAD` button
12. Restart Home Assistant

### Manually:

1. Copy `open_epaper_link` folder from [latest release](https://github.com/jonasniesner/open_epaper_link_homeassistant/releases/latest) to [`custom_components` folder](https://developers.home-assistant.io/docs/creating_integration_file_structure/#where-home-assistant-looks-for-integrations) in your config folder
2. Restart Home Assistant

## Configuration

Adding OpenEPaperLink to your Home Assistant instance can be done via the user interface, by using this My button:

[![image](https://user-images.githubusercontent.com/31328123/189550000-6095719b-ca38-4860-b817-926b19de1b32.png)](https://my.home-assistant.io/redirect/config_flow_start?domain=open_epaper_link)

### Manual configuration steps
If the above My button doesn’t work, you can also perform the following steps manually:

1. Browse to your Home Assistant instance
2. In the sidebar click on  Settings
3. From the configuration menu select: Devices & Services
4. In the bottom right, click on the `Add Integration` button
5. From the list, search and select “OpenEPaperLink”
6. Follow the instructions on screen to complete the setup


