# Community Outreach Drafts

Landing page to share:

```text
https://litime-gateway.tjt-media.online
```

Project repo:

```text
https://github.com/TristanEDU/litime-esp32-gateway
```

Posting approach:

- Be transparent that this is your open-source project.
- Post only where project/self-promotion rules allow it.
- If a community dislikes standalone project posts, use the shorter reply draft only when someone is already asking about LiTime Bluetooth monitoring, remote battery visibility, or ESP32 battery projects.
- Do not imply this is a safety system or a replacement for a shunt, BMS, fuse, charger, or disconnect.
- Lead with what people can do, not hype.

## Source Notes

These communities were selected because recent or indexed discussions mention LiTime batteries, Bluetooth battery monitoring, RV/van solar, Victron/LiFePO4 setups, or marine trolling batteries.

- LiTime official Linktree links to its social accounts and an official group: https://linktr.ee/litime
- Reddit r/SolarDIY has LiTime reliability and Bluetooth/cell-voltage discussion: https://www.reddit.com/r/SolarDIY/comments/1rrmf03/litime_batteries_are_they_actually_reliable_for_a/
- Reddit r/VanLife has LiTime Bluetooth battery troubleshooting: https://www.reddit.com/r/VanLife/comments/1lffaa2
- Reddit r/RVLiving has LiTime RV battery purchase discussion: https://www.reddit.com/r/RVLiving/comments/1rgie1f/cant_decide_which_lithium_battery_to_go_with_i/
- Reddit r/GoRVing has recent LiTime RV battery mentions: https://www.reddit.com/r/GoRVing/comments/1v5rdsp/ready_to_purchase_li_battery_for_rv/
- Reddit r/Victron includes LiTime batteries in a Victron system thread: https://www.reddit.com/r/Victron/comments/1icr46d
- Reddit r/kayakfishing has LiTime trolling-motor battery discussion: https://www.reddit.com/r/kayakfishing/comments/1rr9um3/trolling_motor_batteries/
- Reddit r/jonboats has LiTime Bluetooth trolling battery discussion: https://www.reddit.com/r/jonboats/comments/1tqf9cn/battery_upgrade_suggestions/
- Reddit r/boating has LiTime marine lithium battery discussion: https://www.reddit.com/r/boating/comments/1s7wtwm/lithium_battery_for_jon_boat/
- DIY Solar Power Forum has budget smart LiFePO4 and ESP32/Bluetooth-adjacent threads: https://diysolarforum.com/
- Victron Community has LiTime Bluetooth battery upgrade questions: https://community.victronenergy.com/t/need-help-selecting-victron-equipment-when-upgrading-from-agm-to-lifepo4-batteries/14101
- RVForums has recent LiTime Bluetooth battery discussion: https://rvforums.com/threads/litime-over-charge-protection.22765/
- Forest River Forums has LiTime Bluetooth references in lithium battery upgrade threads: https://www.forestriverforums.com/threads/litium-battery-upgrade-lifep04-litium.1011247/
- iRV2 has LiTime lithium battery discussion: https://www.irv2.com/forums/f56/litimes-new-lithium-batteries-646420-2.html
- Alliance RV Owners Forum has recent LiTime installation discussion: https://alliancervowners.com/forum/threads/lithium-battery.3569/
- BassResource has a LiTime Bluetooth LiFePO4 battery thread: https://www.bassresource.com/bass-fishing-forums/topic/270344-litime-12v-100ah-group-27-bluetooth-lifepo4-battery/
- Sailboat Owners has LiTime-related LFP house battery discussion: https://forums.sailboatowners.com/threads/new-lfp-house-battery.1249942167/page-2
- In-Depth Outdoors has a LiTime lithium battery thread: https://www.in-depthoutdoors.com/community/forums/topic/litime-lithium-batteries/

## General Standalone Post

Title:

```text
I built an open-source ESP32 web dashboard for Bluetooth LiTime batteries
```

Body:

```text
I’ve been working on an open-source ESP32 gateway for Bluetooth LiTime batteries and wanted to share it with people who might actually use or improve it.

What it does:
- Reads LiTime battery telemetry over Bluetooth
- Serves a local browser dashboard from the ESP32
- Keeps a setup Wi-Fi access point available
- Can publish a read-only remote dashboard through a Cloudflare Worker
- Does not require router port forwarding
- Does not expose battery controls

The goal is simple: make it easy to check voltage, current, state of charge, capacity, temperatures, and cell voltages from a browser, especially when the battery is in an RV, van, boat, shed, or off-grid box.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

I wrote the setup guide for beginners, starting at repo download and ending at the Cloudflare remote dashboard. I’d especially appreciate feedback from people with LiTime Bluetooth batteries in real RV, marine, and solar setups.

Quick safety note: this is monitoring only. It is not a BMS, shunt replacement, disconnect, charger controller, or safety system.
```

Short reply version:

```text
If you’re interested in LiTime Bluetooth battery monitoring, I built an open-source ESP32 gateway that turns the battery data into a local web dashboard and optional Cloudflare remote dashboard. It is read-only and does not require router port forwarding:

https://litime-gateway.tjt-media.online

Repo:
https://github.com/TristanEDU/litime-esp32-gateway
```

## Reddit: r/SolarDIY

Title:

```text
Open-source ESP32 dashboard for Bluetooth LiTime batteries
```

Body:

```text
I built a small open-source ESP32 gateway for Bluetooth LiTime batteries and thought r/SolarDIY might be a good place to sanity-check it.

The project reads LiTime BLE telemetry and serves it as a local web dashboard. There is also an optional Cloudflare Worker relay so you can view the battery remotely without exposing the ESP32 or opening router ports.

Why it may be useful here:
- Browser view of LiTime battery status
- Cell voltage list, SOC, current, voltage, temperatures, and capacity
- Local-first setup from the ESP32 access point
- Remote view is read-only
- Beginner setup guide included

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

I know a shunt is still the right tool for system-level accounting. This is meant to expose the battery’s own Bluetooth telemetry in a more useful place, not replace proper system monitoring or protection.
```

## Reddit: r/Victron

Title:

```text
ESP32 read-only web dashboard for Bluetooth LiTime batteries
```

Body:

```text
For anyone using LiTime batteries alongside Victron gear, I built an open-source ESP32 gateway that reads the LiTime Bluetooth telemetry and shows it on a local web dashboard.

It is not trying to replace a SmartShunt, Cerbo, or proper Victron monitoring. The narrow use case is: “I want the LiTime battery’s own Bluetooth data visible in a browser, and optionally available remotely, without opening router ports.”

What it does:
- LiTime BLE telemetry to ESP32
- Local web dashboard
- Optional read-only Cloudflare remote dashboard
- No battery control commands
- No public ESP32 endpoint

Landing page:
https://litime-gateway.tjt-media.online

Repo:
https://github.com/TristanEDU/litime-esp32-gateway

I’d be interested in feedback from people who have mixed budget Bluetooth batteries with Victron systems.
```

## Reddit: r/VanLife

Title:

```text
I made an ESP32 web dashboard for Bluetooth LiTime van batteries
```

Body:

```text
I built an open-source ESP32 project for Bluetooth LiTime batteries that may be useful for van builds where the house battery is tucked away under a bench or cabinet.

The ESP32 reads the LiTime battery over Bluetooth and gives you a local web dashboard. If you want remote access, there is an optional Cloudflare Worker dashboard that the ESP32 connects to outbound, so you do not need port forwarding.

Useful bits:
- Check SOC, voltage, current, temperatures, and cell voltages from a browser
- Local setup Wi-Fi from the ESP32
- Beginner-friendly setup guide
- Remote dashboard is read-only
- No charge/discharge controls exposed

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

This is not a safety system or shunt replacement. It is a way to make the battery’s own Bluetooth telemetry easier to see.
```

## Reddit: r/vandwellers

Title:

```text
Open-source LiTime Bluetooth battery monitor for ESP32
```

Body:

```text
I put together an open-source ESP32 gateway for Bluetooth LiTime batteries and wanted to share it with people building electrical systems in vans.

It turns LiTime battery telemetry into a browser dashboard. The ESP32 serves a local page, and there is an optional Cloudflare Worker remote dashboard if you want to check status while away from the van.

The design is intentionally read-only:
- No BMS control
- No charge/discharge control
- No router port forwarding
- Local-first setup from the ESP32 access point

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

I wrote the setup guide for beginners, including flashing the ESP32 and setting up the Cloudflare dashboard.
```

## Reddit: r/RVLiving

Title:

```text
Read-only web dashboard for LiTime Bluetooth RV batteries
```

Body:

```text
I built an open-source ESP32 gateway for Bluetooth LiTime batteries that might be useful for RV house battery setups.

The practical idea: instead of opening the phone app near the battery compartment, an ESP32 reads the battery over Bluetooth and gives you a local web dashboard. If you want remote access, it can connect outward to a Cloudflare Worker so you do not need to expose your RV network.

What you can see:
- SOC
- Voltage/current/power
- Capacity
- Cell voltages
- Temperatures
- Connection/validity state

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

It is monitoring only and not a replacement for safe wiring, fusing, a BMS, or a shunt.
```

## Reddit: r/GoRVing

Title:

```text
Beginner-friendly ESP32 monitor for LiTime RV batteries
```

Body:

```text
For anyone running LiTime Bluetooth batteries in an RV, I made an open-source ESP32 monitor that turns the battery’s Bluetooth data into a web dashboard.

The setup guide is written for a first-time ESP32 user. It walks through downloading the repo, installing Arduino CLI, flashing the board, joining the setup Wi-Fi, and optionally deploying the Cloudflare remote dashboard.

Landing page:
https://litime-gateway.tjt-media.online

Repo:
https://github.com/TristanEDU/litime-esp32-gateway

The remote part is read-only and does not require port forwarding. It is for monitoring, not controlling the battery.
```

## Reddit: r/traveltrailers

Title:

```text
ESP32 browser dashboard for LiTime Bluetooth travel-trailer batteries
```

Body:

```text
I built an open-source ESP32 project for LiTime Bluetooth batteries and wrote a beginner setup guide.

It gives you a local web dashboard for battery status, plus an optional read-only Cloudflare remote dashboard. The ESP32 makes an outbound connection, so you do not need to open ports on a campground/home router.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

It shows SOC, voltage, current, power, temperatures, and cell voltages. It does not expose battery controls.
```

## Reddit: r/kayakfishing

Title:

```text
Open-source web dashboard for Bluetooth LiTime trolling batteries
```

Body:

```text
I built an ESP32 project that reads Bluetooth LiTime battery telemetry and shows it on a browser dashboard. Thought it might be useful for people running LiTime batteries for trolling motors or electronics.

Use case: the battery is in a box or hatch, but you want a cleaner way to see SOC, voltage, current, and cell status than opening the phone app right next to it.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

It is read-only and not a safety system. I would love feedback from anyone using LiTime Bluetooth batteries on small boats or kayaks.
```

## Reddit: r/jonboats

Title:

```text
ESP32 dashboard for LiTime Bluetooth trolling motor batteries
```

Body:

```text
I made an open-source ESP32 gateway for Bluetooth LiTime batteries that may be useful for jon boat trolling motor setups.

It reads the battery over Bluetooth and serves a local web dashboard. You can also set up an optional read-only remote dashboard through Cloudflare if the boat/charger setup is somewhere with Wi-Fi.

Landing page:
https://litime-gateway.tjt-media.online

Repo:
https://github.com/TristanEDU/litime-esp32-gateway

This is monitoring only: SOC, voltage, current, temperatures, and cell voltages. No battery controls.
```

## Reddit: r/boating

Title:

```text
Open-source LiTime Bluetooth battery dashboard for ESP32
```

Body:

```text
I built a small open-source ESP32 project for Bluetooth LiTime batteries and wanted to share it with people running LiFePO4 batteries on boats.

The ESP32 reads the battery’s Bluetooth telemetry and serves a read-only web dashboard. The optional remote dashboard uses Cloudflare and does not require exposing the ESP32 to the internet.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

It is not for starting-battery safety decisions or charge control. It is just a cleaner monitor for the battery’s own telemetry.
```

## DIY Solar Power Forum

Title:

```text
Open-source ESP32 gateway for Bluetooth LiTime battery telemetry
```

Body:

```text
I built an ESP32 gateway for Bluetooth LiTime batteries and would appreciate feedback from the DIY solar crowd.

It reads the LiTime BLE telemetry path and serves a local web dashboard from the ESP32. There is also an optional Cloudflare Worker dashboard for read-only remote viewing without inbound port forwarding.

Project page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

What it is:
- ESP32 firmware
- Local setup AP and local dashboard
- Optional Cloudflare Worker remote dashboard
- Read-only monitoring

What it is not:
- Not a shunt replacement
- Not a BMS replacement
- Not charge/discharge control
- Not a safety disconnect

The setup guide is written for people who have never flashed an ESP32, but the code is open if anyone wants to inspect or improve the BLE handling.
```

## Victron Community

Title:

```text
LiTime Bluetooth telemetry to local web dashboard with ESP32
```

Body:

```text
I built an open-source ESP32 project for LiTime Bluetooth batteries that may be useful in systems where Victron gear handles system monitoring but the battery’s own Bluetooth telemetry is still useful.

The ESP32 reads the LiTime battery over BLE and exposes a local browser dashboard. Optional remote viewing uses a Cloudflare Worker and an outbound ESP32 connection.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

This does not replace SmartShunt/Cerbo monitoring. It is a read-only bridge for the LiTime battery’s own telemetry: SOC, voltage, current, capacity, temperatures, and cell voltages.
```

## RVForums

Title:

```text
Open-source browser dashboard for LiTime Bluetooth RV batteries
```

Body:

```text
I built an open-source ESP32 gateway for LiTime Bluetooth batteries and thought it may be useful for RV owners using LiTime house batteries.

The ESP32 reads the battery over Bluetooth and serves a local web dashboard. If you want remote viewing, the included Cloudflare Worker dashboard is read-only and does not require port forwarding.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

The project is monitoring only. It shows battery status but does not control the battery, charger, inverter, or RV electrical system.
```

## Forest River Forums

Title:

```text
LiTime Bluetooth battery web dashboard for RV setups
```

Body:

```text
For Forest River owners using or considering LiTime Bluetooth batteries, I built a small open-source ESP32 gateway that turns the battery’s Bluetooth data into a local web dashboard.

It can also publish to an optional read-only Cloudflare remote dashboard without opening router ports.

Landing page:
https://litime-gateway.tjt-media.online

Repo:
https://github.com/TristanEDU/litime-esp32-gateway

This is not a safety device or control system. It is just a way to make SOC, voltage, current, temperatures, and cell voltages easier to see.
```

## iRV2

Title:

```text
ESP32 monitor for LiTime Bluetooth lithium batteries
```

Body:

```text
I wanted an easier way to view LiTime Bluetooth battery data from a browser, so I built an open-source ESP32 gateway.

It serves a local dashboard and can optionally connect outward to a Cloudflare Worker for remote read-only viewing. No inbound port forwarding is needed.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

The setup guide is written for beginners, including flashing the ESP32 and setting up the remote dashboard. Monitoring only, no battery controls.
```

## Alliance RV Owners Forum

Title:

```text
Read-only LiTime Bluetooth battery dashboard for RV owners
```

Body:

```text
I built an open-source ESP32 gateway for LiTime Bluetooth batteries that may help RV owners who want a browser dashboard for house battery status.

It reads LiTime BLE telemetry, serves a local dashboard, and optionally provides a Cloudflare remote dashboard without exposing the ESP32 to the internet.

Landing page:
https://litime-gateway.tjt-media.online

Repo:
https://github.com/TristanEDU/litime-esp32-gateway

It is monitoring only and not a replacement for fusing, shunts, chargers, disconnects, or the BMS.
```

## BassResource

Title:

```text
ESP32 web dashboard for LiTime Bluetooth trolling motor batteries
```

Body:

```text
I built an open-source ESP32 project that reads Bluetooth LiTime battery telemetry and shows it on a web dashboard.

For fishing setups, the use case is simple: if the LiTime battery is in a compartment or battery box, this gives you a browser-based view of SOC, voltage, current, temperatures, and cell voltages.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

It is read-only. No trolling motor control, no charger control, no battery control.
```

## Sailboat Owners

Title:

```text
Open-source ESP32 monitor for LiTime Bluetooth house batteries
```

Body:

```text
I built a small open-source ESP32 gateway for Bluetooth LiTime batteries that may be useful for house battery monitoring on boats.

It reads the battery’s BLE telemetry and serves a local dashboard. Optional remote viewing is handled by a Cloudflare Worker over an outbound ESP32 connection, so no inbound port forwarding is needed.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

It is a monitor only, not a safety system or shunt replacement.
```

## In-Depth Outdoors

Title:

```text
LiTime Bluetooth battery web dashboard for boats and trolling setups
```

Body:

```text
I built an open-source ESP32 project for Bluetooth LiTime batteries that might interest people running LiTime lithium batteries for trolling motors or boat electronics.

The ESP32 reads the battery over Bluetooth and gives you a browser dashboard. There is also an optional read-only remote dashboard through Cloudflare.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

It shows battery telemetry only: SOC, voltage, current, temperatures, capacity, and cell voltages.
```

## LiTime Official Group

Title:

```text
Open-source ESP32 web dashboard for LiTime Bluetooth batteries
```

Body:

```text
I built an independent open-source ESP32 gateway for LiTime Bluetooth batteries and wanted to share it with other LiTime owners.

It reads LiTime battery telemetry over Bluetooth and turns it into a local browser dashboard. There is also an optional Cloudflare Worker dashboard for read-only remote viewing without router port forwarding.

Landing page:
https://litime-gateway.tjt-media.online

GitHub:
https://github.com/TristanEDU/litime-esp32-gateway

The setup guide is written for beginners and starts from downloading the repo. This is monitoring only, not a battery control or safety system.
```
