# UptimeRobot Add-on (more_page)
UptimeRobot dashboard Home Assistant Dwains Dashboard

### Prerequisite
- Make a free [UptimeRobot](https://uptimerobot.com/) account and config what you whant to monitor 
- Make sure you have installed the lovelace [uptime-card](https://github.com/dylandoamaral/uptime-card) 
- Make the intergration with [UptimeRobot in Home Assistant](https://www.home-assistant.io/integrations/uptimerobot/)

### Installation
- Add the [F1 2021 Calendar by Racefans](https://www.racefans.net/contact/f1-fanatic-calendar/) to your Google Calendar
- If you don't have the [Google Calendar Event](https://www.home-assistant.io/integrations/calendar.google/) integration setup yet, make sure to do so. If you already have, please ignore this step.
- Restart home-assistant and open `google_calendars.yaml`, this file should be in the root folder (this is also where your configuration.yaml and secrets.yaml should be located)
- Find the calendar with device id `formula_1_calendar_by_racefans_net`, it should look like this;
```yaml
- cal_id: ekqk1nbdusr1baon1ic42oeeik@group.calendar.google.com
  entities:
  - device_id: formula_1_calendar_by_racefans_net
    ignore_availability: true
    name: Formula 1 calendar by RaceFans.net
    track: true
``` 
