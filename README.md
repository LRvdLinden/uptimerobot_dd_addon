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
