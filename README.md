# linear-gauge-card

![pm2_5_demo](https://github.com/smolbun/linear-gauge-card/assets/45829953/ac28b47a-461c-4cbd-a9db-0a67ed9d362a)

**Options**
| Name | Type | Requirement | Description | Default |
| -------------- | ----------- | ------------ | ------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `type` | string | **Required** | `custom:linear-gauge-card` |
| `entity` | string | **Required** | `sensor.pm2_5_sensor` |
| `name` | string | **Optional** | The title of the card | Device Friendly Name |
| `unit` | string | **Optional** | Display unit alongside the data |
| `fontSize` | string | **Optional** | Font size of the data label and marker | 15px
| `barWidth` | string | **Optional** | Width of the pointer bar | 1%
| `dataLabelColor` | string | **Optional** | Adjust color and/or transparency of the data label | rgba(145, 145, 145, 0.4)
| `dataLabelTextColor` | string | **Optional** | Adjust color of the data label text | white
| `gridLabelTextColor` | string | **Optional** | Adjust color of the grid label text | white
| `start` | integer | **Optional** | The starting value of the segment |
| `startVisibility` | string | **Optional** | Visibility of the starting value | hidden
| `segments` | string | **Required** | Specify the color and how long each data segments will be |
| `until` | integer | **Required** | The length of the segment |


**Example**
```yaml
type: custom:linear-gauge-card
entity: sensor.pm2_5_sensor
name: Living Room PM2.5 (µg/m3)
segments:
  - until: 12
    color: '#43A047'
  - until: 35
    color: '#FFC730'
  - until: 55
    color: '#FF8000'
  - until: 100
    color: '#DB4437'
```
```yaml
type: custom:linear-gauge-card
entity: sensor.aq_sensor_co2
name: SCD40 C02
fontSize: 15px
start: 400
startVisibility: visible
segments:
  - until: 1000
    color: "#43A047"
  - until: 1400
    color: "#FFC730"
  - until: 2000
    color: "#DB4437"
```
