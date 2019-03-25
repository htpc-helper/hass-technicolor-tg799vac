# hass-technicolor-tg799vac
- Home Assistant sensor plugin for Technicolor TG799vac modem
- Modem has been modified with https://github.com/davidjb/technicolor-tg799vac-hacks
- May work with other similar modems
- May *not* work if the TG799vac has been flashed with 3rd party firmware which has altered the code for the web ui which this script scapes.
- Based on the work of Matt Johnston with https://github.com/mkj/tgiistat
- htpc-helper (c) 2018

## Installation

1. Install this sensor by creating a custom_components folder in the root directory where your `configuration.yaml` file is located *(if you don't already have one)*.
2. Inside the `custom_components` folder create another folder named `technicolormodem`. Copy the `sensor.py` file you downloaded from this repository into this folder *(if you copy and paste the code, ensure you do so from the [raw version](https://raw.githubusercontent.com/htpc-helper/hass-technicolor-tg799vac/master/custom_components/technicolormodem/sensor.py))*.
3. Add the following code to your `configuration.yaml` using the example below. Further customisation can be made, please refer to the table below.
4. **You'll need to restart after installation for the sensor to appear in Home Assistant.**

#### Usage

To use this sensor in your installation, add the following to your `configuration.yaml` file:

``` yaml
platform: technicolormodem
host: IP_ADDRESS
monitored_variables:
- dsl_status
- dsl_uptime
- uptime
- up_speed
- down_speed
- up_maxspeed
- down_maxspeed
```

#### Configuration variables:
| Key | Type | Required | Default | Description |
| :--- | :--- | :--- | :--- | :--- |
| `platform` | `string` | `True` | `technicolormodem` | Sensor platform name.
| `name ` | string | `False` | `TechnicolorModem` | Name of the sensor.
| `host` | string | `True` | test | The hostname or IP address where your modem can be reached.
| `scan_interval` | number | `False` | `60` | Number of seconds between polls. Default `60`
| `monitored_variables` | list | False | `None` | `up_speed`, `down_speed`, `up_maxspeed`, `down_maxspeed`, `up_power`, `down_power`, `up_noisemargin`, `down_noisemargin`, `up_attenuation1`, `up_attenuation2`, `up_attenuation3`, `down_attenuation1`, `down_attenuation2`, `down_attenuation3`, `dsl_uptime`, `dsl_mode`, `dsl_type`, `dsl_status`, `product_vendor`, `product_name`, `software_version`, `firmware_version`, `hardware_version`, `serial_number`, `mac_address`, `uptime`





## Contributing
See [here](https://github.com/htpc-helper/hass-technicolor-tg799vac/blob/master/CONTRIBUTING.md)
