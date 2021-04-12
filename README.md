# UptimeRobot Add-on (more_page)
UptimeRobot dashboard Home Assistant Dwains Dashboard

### Prerequisite
- Make a free [UptimeRobot](https://uptimerobot.com/) account and config what you whant to monitor 
- Make sure you have installed the lovelace [uptime-card](https://github.com/dylandoamaral/uptime-card) and [fontawesome icons](https://github.com/thomasloven/hass-fontawesome)
- Make the intergration with [UptimeRobot in Home Assistant](https://www.home-assistant.io/integrations/uptimerobot/)
- Restart Home Assistant

### Installation Add-on
- Copy the `page.yaml` file in to a new created folder in `dwains-dashboard/addons/more_page/uptime` directory.
- Open your `more_page.yaml` file in `dwains-dashboard/configs` and add the following;
 ```yaml
     - name: UptimeRobot
       icon: fas:cloud-upload-alt
       path: 'dwains-dashboard/addons/more_page/uptime/page.yaml'
```
- Reload the theme configuration via Theme Settings

### Change code
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
