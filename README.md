# UptimeRobot Add-on (more_page)
UptimeRobot dashboard Home Assistant Dwains Dashboard

### Prerequisite
- Make a free [UptimeRobot](https://uptimerobot.com/) account and config what you want to monitor 
- Make sure you have installed the lovelace [uptime-card](https://github.com/dylandoamaral/uptime-card) and [fontawesome icons](https://github.com/thomasloven/hass-fontawesome)

### Make Home Assistant intergration 
- Make the intergration with [UptimeRobot in Home Assistant](https://www.home-assistant.io/integrations/uptimerobot/)
- Restart Home Assistant
 ```yaml
     # Example configuration.yaml entry
     binary_sensor:
       - platform: uptimerobot
         api_key: YOUR_API_KEY
```

### Installation Add-on
- Copy the `uptimerobot` folder in to the `dwains-dashboard/addons/more_page` directory.
- Open your `more_page.yaml` file in `dwains-dashboard/configs` and add the following;
 ```yaml
     - name: UptimeRobot
       icon: fas:cloud-upload-alt
       path: 'dwains-dashboard/addons/more_page/uptimerobot/page.yaml'
```
- Reload the theme configuration via Theme Settings

### Replace the following;
 ```yaml
     - type: 'custom:uptime-card'
       entity: binary_sensor. # <-vul de sensor aan
       icon: 'fas:safari'
       name: cloud.....nl
       hours_to_show: 72
       status_adaptive_color: true
       average_text: '% uptime'
         alias:
           ok: Online
           ko: Offline
         color:
           icon: white
           ok: '#45C669'
           ko: '#C6B145'
           half: '#C66445'
           none: '#C9C9C9'
           title: white
         show:
           header: true
           title: true
           icon: true
           footer: true
           status: true
           timeline: true
           average: true
         tooltip:
            animation: true
          #tap_action:
            #action: url
            #url: 'https://'
```
- add the correct `binary_sensor` to monitor
- fill in the correct `name:`
- add the `icon:` that you want to have
- when you want to use the `tap-action` function, delete `#` and fill in the `url: 'https/'` to the function
- when you want to monitor shorter or longer then 3 days, change the value `hours_to_show:`
- copy the above string as muth as you need for each `binary_sensor`

### Result;
- ![uptimerobot](https://user-images.githubusercontent.com/77990847/114383489-e59e8f80-9b8d-11eb-838f-a3caa9539f61.png)
