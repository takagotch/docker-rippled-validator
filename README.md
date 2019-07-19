### docker-rippled-validator
---
https://github.com/WietseWind/docker-rippled-validator

```
```

```sh
docker build --tag rippledvalidator:latest .
docker run -dit \
  --name rippledvalidator \
  -p 51235:51235 \
  -v /My/Local/Disk/RippledKeystore/:/keystore/ \
  xrptipbot/rippledvalidator:latest
  
docker exec rippledvalidator cat /root/.ripple/validator-keys.json|grep public_key
docker logs -f rippledvalidator
docker exec rippledvalidator server_info
/opt/ripple/bin/rippled server_info -q | grep pubkey_validator
```

```
```


