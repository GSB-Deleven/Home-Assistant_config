# Setup Guide (WorkInProgress)

* Setup Raspberry Pi 
    * https://www.home-assistant.io/getting-started/
* Setup Active Backup for Business on Synology, so you have a automated local backup, just to be sure 
    * I added it as a File Server
    * Add samba credentials, not the ones from Home-Assistant or NAS
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
email: YOUR.EMAIL@HERE.com
domains:
  - YOUR_DOMAIN.com
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
    * If everything is ok, reboot

* Connect to GitHUB
    * Download and open GitHub Desktop
    * Add existing repository
    * point it to your live folder where your `configuration.yaml`file is
    *   it will say that it isnt a Git repository, but there is a small link in the text above it, to make it a Git repository, called `create a repository here`, click that
    * follow the rest of the instructions
    * commit the changes
    * make sure the `.gitignore`is up to date and has the `secrets.yaml`file in it. (it should be, if you followed the steps above)
    * push it to GitHub

<<<<<<< HEAD
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
=======
* [In this Project](https://github.com/GSB-Deleven/Home-Assistant_config/projects/3) you see what else I installed

* [In the Wiki](https://github.com/GSB-Deleven/Home-Assistant_config/wiki) I explaine the things which need explanation (mostly because I struggled myself during the Install)

* If you would like something else explained, let me know [here in a Disussion](https://github.com/GSB-Deleven/Home-Assistant_config/discussions?discussions_q=category%3ARequest)

>>>>>>> 6e4099279b92afd54ec29d5f240c8154a05abad8

