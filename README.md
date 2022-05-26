## What?

gl-inet distro for TP-Link MR3020 v3. Limited space so limited features:
- 4G, USB tethering and repeater mode supported
- Wireguard supported (client mode only)
- English only, other languages removed
- no opkg
- no QoS, IPv6, OpenVPN, cloud integration
- no USB storage support

## Latest build
[![build status](https://github.com/bogsen/glinet-mr3020/actions/workflows/build.yml/badge.svg)](https://github.com/bogsen/glinet-mr3020/actions/workflows/build.yml)

## How to build
Using CI workflow:
```
$ brew install act
$ act --artifact-server-path artifacts --env GITHUB_RUN_ID=$(date +%s) --reuse
```

Using gl_imagebuilder:
```
$ docker run --rm -v "$(pwd)":/src --entrypoint gl_imagebuilder/gl_image gl_imagebuilder --ignore --config images.json --profile tl-mr3020-v3
```
