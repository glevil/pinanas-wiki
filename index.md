# PiNanas

## I. Description

PiNanas is a personnal cloud server, media center and home-hosted set of services designed to run on a small computer like a Raspberry Pi.

Features include:
- DHCP server **_(DHCPD)_**
- reverse proxy **_(Traefik)_**
- two-factor and SSO authentification server **_(Authelia)_**
- network-wide software for blocking ads & tracking **_(AdGuard Home)_**
- resource monitoring **_(Netstat)_**
- application dashboard **_(Heimdall)_**
- Personnal cloud server **_(Nextcloud)_**
- Media-center **_(Jellyfin)_**
- ...

## II. Installation

### Requirements

#### Hardware

PiNanas will need a linux-based host, with:

- 10 GB free disk space
- 4 GB RAM _(8 GD recommanded)_
- An access to internet
- Optionnaly: a GPU suited to your needs (video transcoding & playing)

#### Software

During installation or operation, PiNanas requires:

- GNU utils
- python3 and pip
- docker and docker-compose
- a wildcard (sub)domain name (e.g `*.home.example.com`)

### Download

#### Via git

From your PiNanas host, anywhere:

``` markdown

git clone --depth 1 --branch develop https://github.com/yscialom/pinanas.git

```

#### Direct download

Go and download our [lastest release](https://www.pinanas.com). Unzip it anywhere

### Settings

Create the installation directory for PiNanas, e.g. in /opt/pinanas and go there:

``` markdown

sudo mkdir -p /opt/pinanas
sudo chown [user]:[user_group] /opt/pinanas
cd /opt/pinanas

```
Define your settings

Fulfil the settings file from template
If you need help, read the [settings man page]

``` markdown

cp /path/to/downloaded/pinanas/src/settings.yml.sample settings.yml
chmod 600 settings.yml
nano settings.yml

```

### Install

From your installation directory, run the configuration script:

``` markdown

/path/to/downloaded/pinanas/src/configure.sh

```

Your installation is now complete.

Any troubles ? Maybe read the [settings man page] and re-run the script.


If you made important changes and want to regenerate PiNanas, run with `--force`.

# III. Start

Ready ?

From your installation directory, run `docker-compose up -d`
