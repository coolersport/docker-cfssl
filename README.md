# docker-cfssl
Collection of cfssl utilities

```
cat <<EOF | docker run -i -v `pwd`:/data -u $(id -u):$(id -g) coolersport/cfssl cfssl genkey - | docker run -i -v `pwd`:/data -u $(id -u):$(id -g) coolersport/cfssl cfssljson -bare server
{
  "hosts": [
    "domain1.com",
    "domain2.com"
  ],
  "CN": "domain1.com",
  "key": {
    "algo": "ecdsa",
    "size": 256
  }
}
EOF
```
