
**Creating server**
```shell
docker-compose run --rm openvpn ovpn_genconfig -u udp://<ip_address or domain>
docker-compose run --rm openvpn ovpn_initpki
```

**Run server** 
```shell
docker-compose up -d openvpn
```

**New client**
```shell
docker-compose run --rm openvpn easyrsa build-client-full <client_name> nopass  
docker-compose run --rm openvpn ovpn_getclient <client_name> > <client_name>.ovpn  
```