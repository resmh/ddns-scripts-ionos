# ddns-scripts-ionos
The script at hand permits to use the IONOS DNS API in order to configure dynamic addresses. Please note: IONOS is a registered trademark of IONOS SE. The script is neither affiliated with nor approved by IONOS SE.

## Usage
Follow the official usage guide to obtain the access token to be pasted as password. Optionally set additional parameters to ```privatedual``` in order to add the selected interface's IPv4 address to the DNS record.

## Status
Please note: This application has been subjected to non-exhaustive internal tests and is therefore **not** cleared for productive use. Please verify against the terms of API usage whether it is permitted.

## Manual Updates
```opkg install https://github.com/resmh/ddns-scripts-ionos/releases/download/latest/ddns-scripts-ionos.ipk```

## Automatic Updates
Add repository, add repository key, update package lists and install:

```
echo 'src ddns_scripts_ionos https://github.com/resmh/ddns-scripts-ionos/releases/download/latest' >> /etc/opkg/customfeeds.conf; \
wget -O /tmp/ddns_scripts_ionos https://github.com/resmh/ddns-scripts-ionos/releases/download/latest/ddns_scripts_ionos.signify.pub; \
opkg-key add /tmp/ddns_scripts_ionos; \
rm /tmp/ddns_scripts_ionos; \
opkg update; \
opkg install ddns-scripts-ionos
```
