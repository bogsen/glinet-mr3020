## What?

gl-inet distro for TP-Link MR3020. Limited space so limited features:
- 4G, USB tethering and repeater mode supported
- Wireguard supported (client mode only)
- English only, other languages removed
- no opkg
- no QoS, IPv6, OpenVPN, cloud integration
- no USB storage support

## How to build
```
docker run --rm -v "$(pwd)":/src --entrypoint gl_imagebuilder/gl_image gl_imagebuilder --ignore --config images.json --profile tl-mr3020-v3
```

