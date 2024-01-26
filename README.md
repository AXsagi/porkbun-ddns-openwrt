# Porkbun ddns update script that supports OpenWRT

## Requirements
`curl ddns-scripts luci-app-ddns curl jq coreutils`

## Installation
```
opkg update
opkg install curl ddns-scripts luci-app-ddns curl jq coreutils
curl -o /etc/ddns/porkbun-ddns.sh https://raw.githubusercontent.com/AXsagi/porkbun-ddns-openwrt/main/porkbun-ddns.sh
chmod +x /etc/ddns/porkbun-ddns.sh
vim /etc/ddns/porkbun-ddns.sh
```

### In the vim editor you must edit the following variables
#### `apikey, apisec`: Enter the details from the API Generation page in Porkbuns website
#### `domain`: The domain in porkbun in which you want to edit its records
#### `record`: The specific record in that domain specified above that you want to update its records

## Setup in OpenWRT DDNS service
<img width="948" alt="image" src="https://github.com/AXsagi/porkbun-ddns-openwrt/assets/60316868/6ffbfbfb-69e7-4938-b656-d157055b05e1">


Many thanks to [krraaamer/porkbun-ddns.sh](https://github.com/krraaamer/porkbun-ddns.sh) for the original code
