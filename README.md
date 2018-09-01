# Sonarr Upcoming Media Component

Component required to use the associated Lovelace card: [Upcoming_Media_Card](https://github.com/custom-cards/upcoming-media-card)</br>
This is just a modified version of home assistants default sonarr component.</br>
This component works with or without the default sonarr component.</br></br>
<link href="https://fonts.googleapis.com/css?family=Lato&subset=latin,latin-ext" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/FgwNR2l"><img src="https://www.buymeacoffee.com/assets/img/BMC-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:5px">If you feel I deserve it, you can buy me a coffee</span></a>

## Installation:

1. Install this component by copying to your `/custom_components/sensor/` folder.
2. Add this to your `configuration.yaml` using the config options below example. 
3. **You will need to restart for the component to start working.**

```
sensor:
- platform: sonarr_upcoming_media
  api_key: YOUR_API_KEY
  host: 192.168.1.4
  port: 8989
  days: 2
  ssl: true
```

### Options

| key | default | required | description
| --- | --- | --- | ---
| api_key | | yes | Your Sonarr API key
| host | localhost | no | The host Sonarr is running on.
| port | 8989 | no | The port Sonarr is running on.
| urlbase | / | no | The base URL Sonarr is running under.
| days | 7 | no | How many days to look ahead for the upcoming sensor, 1 means today only.
| ssl | False | no | Whether or not to use SSL for Sonarr. Set to `True` if you use SSL.

## Developers

**If you'd like to make your own component to feed the upcoming media card:**

1. Make a sensor that follows this naming convention "sensor.sonarr_upcoming_media", replacing sonarr with your service.
2. The state of the sensor must be the amount of items (episodes, movies, etc.) to be listed.
3. The card looks for numbered attributes with values formatted like this example:

```
banner1: https://www.thetvdb.com/banners/graphical/5b43a197b530e.jpg
poster1: https://www.thetvdb.com/banners/_cache/posters/290853-15.jpg
title1: Fear the Walking Dead
subtitle1: Weak
airdate1: 2018-09-02
airtime1: 21:00
hasFile1: false
info1: S01E01
banner2: https://www.thetvdb.com/banners/graphical/239851-g.jpg
poster2: https://www.thetvdb.com/banners/_cache/posters/239851-2.jpg
title2: Penn & Teller: Fool Us
subtitle2: The Fool Us Zone
airdate2: 2018-09-03
airtime2: 20:00
hasFile2: false
info2: S07E11
```

Then all the user needs to do is put your service name in the config like so "service: sonarr".</br>
Please inform me if you create one and I'll add it to the list.</br>
If you need special styling or edits to the card to accomidate your service, just ask or submit a PR.</br></br>

Thanks!
