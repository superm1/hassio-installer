[![Build Status](https://dev.azure.com/home-assistant/Home%20Assistant/_apis/build/status/home-assistant.hassio-installer?branchName=master)](https://dev.azure.com/home-assistant/Home%20Assistant/_build/latest?definitionId=6&branchName=master)

# Install Hass.io

Beside the usage of the images it's also possible to run Hass.io on a generic system without flashing an image.

## Requirements

```
docker-ce
bash
jq
curl
avahi-daemon
dbus
```

## Optional

```
apparmor-utils
```

## Run

Run as root (sudo su):

```bash
curl -sL https://raw.githubusercontent.com/home-assistant/hassio-installer/master/hassio_install.sh | bash -s
```

### Command line arguments
| argument           | default                                                                                                                                                                             | description                                            |
|--------------------|-------------------|--------------------------------------------------------|
| -m \| --machine    |                   | On a special platform they need set a machine type use |
| -d \| --data-share | /usr/share/hassio | data folder for hass.io installation                   |

you can set these parameters by appending ` -- <parameter> <value>` like:

```bash
curl -sL https://raw.githubusercontent.com/home-assistant/hassio-installer/master/hassio_install.sh | bash -s -- -m MY_MACHINE
```

## Supported Machine types

- intel-nuc
- odroid-c2
- odroid-xu
- orangepi-prime
- qemuarm
- qemuarm-64
- qemux86
- qemux86-64
- raspberrypi
- raspberrypi2
- raspberrypi3
- raspberrypi3-64
- tinker
