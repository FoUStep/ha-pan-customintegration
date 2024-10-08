<sub>Fork of [Skalavala's version](https://github.com/skalavala/mysmarthome), which unfortunately no longer has the code available.</sub>

| @8th October 2024 | Version |
|---------------:|----------|
| Tested on      |  PA-440 |
| PAN-OS         |  11.2.3 |
| Home Assistant | 2024.10.1 |

<br><br>
[![GitHub release](https://img.shields.io/github/release/FoUStep/ha-pan-customintegration.svg)](https://GitHub.com/FoUStep/a-pan-customintegration/releases/)

**Setup through HACS instructions**:
1. Add the repository with type Integration:
   https://github.com/FoUStep/ha-pan-customintegration
2. Add to configuration.yaml:
```yaml
  # Palo Alto Networks custom integration
  - platform: paloalto
    api_key: !secret paloalto_authkey
    ip_address: !secret paloalto_hostip
    monitored_conditions:
      - host_name
      - up_time
      - serial_no
      - sw_version
      - gp_version
      - logdb_version
      - operation_mode
      - cpu_temp
      - gp_users
      - gp_user_count
      - loggedin_user_count
      - loggedin_users
```
3. Allow PA API access and get the API key and management IP.
4. Add paloalto_authkey and paloalto_hostip to secrets.yaml.
5. Restart Home Assistant.

**Manual setup instructions**:
1. Upload folder including all files to /config/custom_components/ on Home Assistant host.
2. Add to configuration.yaml:
```yaml
  # Palo Alto Networks custom integration
  - platform: paloalto
    api_key: !secret paloalto_authkey
    ip_address: !secret paloalto_hostip
    monitored_conditions:
      - host_name
      - up_time
      - serial_no
      - sw_version
      - gp_version
      - logdb_version
      - operation_mode
      - cpu_temp
      - gp_users
      - gp_user_count
      - loggedin_user_count
      - loggedin_users
```
3. Allow PA API access and get the API key and management IP.
4. Add paloalto_authkey and paloalto_hostip to secrets.yaml.
5. Restart Home Assistant.


First repo on GitHub, bare with me.
