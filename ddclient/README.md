# ddclient

 Config file at ```/etc/ddclient/ddclient.conf``` :

```text
#How often to check ip address
daemon=1800

#Use the Cloudflare protocol
protocol=cloudflare

#Tell ddclient to get real ip address
use=web
#web=checkip-dyndns-org/
web-skip='IP Address'
#Credentials for Cloudflare api (Global API key)
ssl=yes
#server=www.cloudflare.com
login=steve@groom.ch
password=<38 char key from Global API key>

zone=grooms.page

#Domain for update
grooms.page,home.grooms.page

```

ddclient checks the local ISP's assigned IP address matches the defined DNS entry. If they differ, then __ddclient__ will use the cloudflare api to update the defined DNS.
