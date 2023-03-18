key phrase: qqqq
key phrase_1: qqqq
ServerName: iredy

Creaating server
```shell
docker-compose run --rm openvpn ovpn_genconfig -u udp://<ip_address or domain>
docker-compose run --rm openvpn ovpn_initpki

docker-compose up -d openvpn

# Создает клиентский сертификат
docker-compose run --rm openvpn easyrsa build-client-full iphone nopass  
docker-compose run --rm openvpn ovpn_getclient iphone2 > iphone2.ovpn  

```