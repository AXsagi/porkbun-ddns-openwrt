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

In the vim editor you must edit the following variables:
apikey, apisec: enter the details from the API Generation page in Porkbuns website
domain: the domain in porkbun in which you want to edit its records
record: the specific record in that domain specified above that you want to update its records
 