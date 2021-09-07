# Ziggo-Remote-Control<br>
Ziggo-Remote-Control for HA<br>
<br>
This Remote is not done yet<br>
but the remote will work in conjunction with<br>
https://github.com/Sholofly/arrisdcx960<br>
<br>
And is based on<br>
https://github.com/madmicio/LG-WebOS-Remote-Control<br>
All the credits for the design go to: madmicio<br>

installation:<br>
HACS:<br>
1. Go to HACS<br>
2. Click FrontEnd http://homeassistant:8123/hacs/frontend<br>
3. Click 3 dots in the top right corner and Select "Custom repositories"<br>
3. Scrol down and Add: <br>
    url: https://github.com/bkbartk/Ziggo-Remote-Control<br>
    category: Lovelace<br>
4. in the dashboard add a Card like the sample below<br>
<br>
MANUAL<br>
1. copy: "ziggo-remote-control.js" to "~\config\www\community\Ziggo-Remote-Control\ziggo-remote-control.js"<br>
 using git or some other method<br>
2. in Ha go to Configuration\Loveace Dashboard\ resources http://homeassistant:8123/config/lovelace/resources<br>
3. click add resource and add: "\hacsfiles\Ziggo-Remote-Control\ziggo-remote-control.js" Javascript Module<br>
4. in the dashboard add a Card like the sample below<br>

Usage Sample: 
```yaml
type: custom:ziggo-remote-control
entity: media_player.mediabox
volumeEntity: media_player.living_room_tv
volumeService: webostv
colors:
  buttons: var(--deactive-background-button-color)
sources:
  - name: Netflix
    icon: mdi:netflix
  - name: Videoland
    icon: mdi:video
  - name: YouTube
    icon: mdi:youtube-tv
```

volume services are separate because the media box does not support this.
if you don't have a supporting tv you should add dummy values.
