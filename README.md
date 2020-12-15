# Home-Assistant on my Synology918+ NAS, running as a VM

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
-------------------------------------------------------------

## Guide (WorkInProgress)

* Setup the VM
    * https://gh2home.nl/homeassistant/install-home-assistant-in-a-virtual-machine-vmm/
* Make a Snapshot of fresh install
* Make IP Static (Router), Port Forward () Router
* Profile -> Advanced Mode
* Supervisor Installs
    * Samba 
        * Configure and Start Service
```yml
workgroup: WORKGROUP
username: YOUR_USERNAME
password: 'YOUR_PASSWORD'
interface: ''
allow_hosts:
  - 10.0.0.0/8
  - 172.16.0.0/12
  - 192.168.0.0/16
  - 'fe80::/10'
  - YOUR_IPs_which_should_be_allowed
  - YOUR_IPs_which_should_be_allowed
  - YOUR_IPs_which_should_be_allowed
  - YOUR_IPs_which_should_be_allowed
veto_files:
  - ._*
  - .DS_Store
  - Thumbs.db
  - icon?
  - .Trashes
compatibility_mode: false
     
```
* DuckDNS (http://deleven.duckdns.org:8123/)
    * Configure and start Service
```yml
lets_encrypt:
  accept_terms: true
  certfile: fullchain.pem
  keyfile: privkey.pem
token: YOUR_TOKEN
domains:
  - YOUR_DOMAIN.duckdns.org
aliases: []
seconds: 300
     
```
* Lets Encrypt
    * Config
```yml
email: david.leuenberger@outlook.com
domains:
  - deleven.duckdns.org
certfile: fullchain.pem
keyfile: privkey.pem
challenge: http
dns: {}
```

* Connect Mac Finder/ Windows explorer to Server via smb
* Copy Custom components folder from previous install
* Reboot  
* If everything runs fine, make a snapshot and download it
* Copy the following codes from GitHub or from previous install/backup etc.
    * `secrets.yaml`
    * `secrets_template.yaml`
    * `scripts.yaml`
    * `scenes.yaml`
    * `groups.yaml`
    * `configuration.yaml`
    * `automations.yaml`
    * `.gitignore`
    * `README.md`
    * `input_select.yaml`
    * `input_number.yaml`
* Create a Dashboard called 
> Deleven
* Check config
    * If Everything is ok, reboot

* Connect to GitHUB
    * Download and open GitHub Desktop
    * Add existing repository
    * point it to your live folder where your `configuration.yaml`file is
    *   it will say that it isnt a Git repository, but there is a small link in the text above it, to make it a Git repository, called `create a repository here`, click that
    * follow the rest of the instructions
    * commit the changes
    * make sure the `.gitignore`is up to date and has the `secrets.yaml`file in it. (it should be, if you followed the steps above)
    * push it to GitHub




* More Supervisor Installs
    * Check Home Assistant configuration
    * SSH & Terminal
    * File Editor
    * Glances
    * AirCast
    * Google Assistant SDK
    * Mosquitto broker MQTT
    * Configure GitHub Auto Backup https://www.youtube.com/watch?v=9-OG3bCQFFQ
    * GitHub integration https://youtu.be/rzE9WXZj6N8

-------------------------------------------------------------
-------------------------------------------------------------
-------------------------------------------------------------
-------------------------------------------------------------
-------------------------------------------------------------
-------------------------------------------------------------
-------------------------------------------------------------
-------------------------------------------------------------
-------------------------------------------------------------
-------------------------------------------------------------

# Old Stuff from the Old README.md

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