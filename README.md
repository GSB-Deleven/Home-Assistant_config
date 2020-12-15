# Home-Assistant-on-DelevenPi4
 My Home Assistant Setup on my Raspberry Pi 4 (8GB), which is running a Minecraft Server at the same time under Ubuntu 20.10

-------------------------------------------------------------

## Will crate a README/GUIDE/"See whats in it" when this thing is running as it should. Currently its just a playground for me
-------------------------------------------------------------

## `secrets.yml` file
for obvious reasons the `secrets.yml` file doesnt get uploaded. (added to .gitignore)  
Just use the `secrets_template.yaml` and copy&paste the structre, so you know how you should build it.
Well what should i say, its a template.

-------------------------------------------------------------

# Things which are installed

## via `configuration.yml`
* Spotify (Local Playback), after the `coniguration.yml`, also needs Integrations Setup
* Radio on Google Home
* Radarr
* Vacuum xiaomi_miio

------------------------------------------------------------------

## via Menu -> Integrations
* brother Printer
* Coronavirus
* Glances
* Global Disaster Alert
* Google Cast
* GPS Logger
* Home Assistant iOS
* HomeKit
* IFTTT
* Internet Printing Protocol (IPP)
* Local IP Address
* Meteorologisk institutt (Met.no)
* Minecraft Server
* Mobile App
* NZBGet
* Profiler
* Raspberry Pi Power Supply Checker
* Shopping List
* Sonarr
* Speedtest.net
* Synology DSM
* UPnP (Router)
* XBOX

------------------------------------------------------------------

## via HACS    

### Integrations
* spotcast
* SamsungTV Tizen (Not Setup yet)
* Monitor Docker (Not Setup yet)
* 

### Frontend
* Mini Graph Card 
* 

------------------------------------------------------------------

# ToDo
- [x] Setup Spotify to Chromecast - See Wiki for instructions how to
- [x] Install HACS (Easy Guide https://hacs.xyz/docs/installation/manual_cli)
- [ ] HACS Cards for Minecraft  
- [ ] HACS Cards for Vaccumcleaner  
- [ ] HACS Cards for NZBGet  
- [ ] HACS Cards for Sonarr  
- [ ] HACS Cards for Radarr  
- [ ] HACS Cards for Home Assistant Spotify Lovelace Card (https://github.com/custom-cards/spotify-card)  
- [ ] Setup Global Disaster Alert and Coordination System (GDACS)  
- [ ] Setup Coronavirus (COVID-19)  
- [ ] Setup GPSLogger  
- [ ] Setup IFTTT  