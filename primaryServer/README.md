# Primary Server

The "primary" server denotes the server where the majority of the work will be done. This should ideally be the highest-spec'ed machine in the setup.

# Packages

|Package|Usage|
|---|---|
|`rsync`|File transfers; faster and safer than `scp`|
|`fish`| Preference; Shell that comes with autofills and reasonable defaults; ***NOT POSIX COMPLIANT***\*|
|`fwupd`| FirmWare Update Program and Daemon|
|`git`| Used for pulling down packages and config files|
|`links`| CLI-mode browser; May also be listed as `links2`|
|`neovim`| Derivative of Vim; text editor|
|`samba`| Server for SMB/Windows Network Drive protocol|
|`zfs`| File system protocol for accessing bulk storage|
|`apcupsd`|APC Uninterruptible Power Supply Daemon; for communicating with UPS|
|`docker`| Most services running on the server run in docker|
|`docker-compose`|Allows for docker configs to be stored in files|
|`openssh`|SSH backend|
|`openssl`|HTTPS library|
|`man-db`|Manual for installed software; Often called "man pages"|

*: "POSIX Compliance" is a standard for most shell programs, like `bash` and `sh`, which allow scripts to run largely regardless of which shell is installed. Some scripts and copy-paste commands expect POSIX compliance, so if/when scripts don't work in `fish`, `bash` is used instead. 

# Services

|Name|Containing folder|Usage|In-use|
|---|---|---|---|
|Audiobookshelf|`audiobook`|Storage and collection of audiobooks, ebooks, and podcasts|✔|
|Mullvad VPN|`automations`|VPN service for other containers|✔|
|QBittorrent|`automations`|Torrent client|✔|
|Sonarr|`automations`|TV series requesting service|✔|
|Radarr|`automations`|Movie requesting service|✔|
|Prowlarr|`automations`|Torrent indexer|✔|
|Bazarr|`automations`|Subtitle requesting service (tied to Sonarr and Radarr)|✔|
|Readarr|`automations`|eBook requesting service|×|
|Pleroma|`blog`|Mastodon/Fediverse client/instance|✔|
|Caddy|`caddy`|Reverse proxy service|✔|
|Factorio|`factorio`|Selfhosted Factorio server|✔|
|Miniflux|`feedReader`|RSS Feed Agregator and reader|✔|
|Forgejo|`gitRepo`|Self-hosted Github alternative|✔|
|Woodpecker|`gitRepo`|CI/CD Frontend|✔|
|Homebox|`inventory`|Inventory management system|×|
|Jellyfin|`jellyfin`|Media and Content viewing server|✔|
|Write-Freely|`journal`|Blogging site|×|
|Ladder|`ladder`|Self-hosted `12ft.io` alternative|✔|
|Flame|`landingPage`|Landing page; link to pages|✔|
|Matrix|`matrix`|Matrix instance and client|×|
|Minecraft|`mainecraft`|Self-hosted Minecraft server|✔|
|Kiwix|`mirrorHosting`|Self-hosted mirrors of popular wiki content|×|
|Prometheus Exporter|`monitoring`|Metrics endpoint for Prometheus|✔|
|cAdvisor|`monitoring`|Container Advisor backend|✔|
|Navidrome|`music`|Music streaming service|×|
|Piwigo|`piwigo`|Self-hosted image server \[paired with MagicMirror]|✔|
|Wekan|`wekan`|Trello alternative|×|
