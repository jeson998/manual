---
sidebar_position: 4
---

# Trojan

## Protocol standard

- https://trojan-gfw.github.io/trojan/protocol
- https://en.wikipedia.org/wiki/Transport_Layer_Security
- https://en.wikipedia.org/wiki/Server_Name_Indication

## Sample

```ini
ProxyTrojan = trojan, 192.168.20.6, 443, password=password1, udp-relay=false, skip-cert-verify=true, sni=www.google.com
```

## Format

```ini
{proxy name} = trojan, {host}, {port}, {password}, {udp-relay}, {skip-cert-verify}, {sni}
```

## Params

| Name             | Value          | Mandatory | Note                                                                       |
|------------------|----------------|-----------|----------------------------------------------------------------------------|
| proxy name       | -              | true      |                                                                            |
| host             | -              | true      | Support domain and ip format                                               |
| port             | 0 - 65535      | true      |                                                                            |
| password         | -              | true      |                                                                            |
| udp-relay        | true<br/>false | false     | Default value: false                                                       |
| skip-cert-verify | true<br/>false | false     | Default value: false<br/>                                                  |
| sni              | -              | false     | Definition is unnecessary when the SNI value is the same as the host value |