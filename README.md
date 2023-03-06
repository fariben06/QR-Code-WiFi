# WiFi-QrCode-Generator

Générez un code QR pour votre réseau WiFi pour permettre aux autres de se connecter rapidement sans avoir à leur dire votre mot de passe long et compliqué.

## Installation

```bash
$ pip install wifi-qrcode-generator
```

## Usage

### Mode interactif

```bash
$ wifi-qrcode-generator
```

![CLI interactive mode](images/CLI%20interactive.png)
![QR Code](images/Home%20WiFi.png)

### Python API

```python
#!/usr/bin/env python3
import wifi_qrcode_generator.generator

qr_code = wifi_qrcode_generator.generator.wifi_qrcode(
    ssid='My awesome WIFI', hidden=False, authentication_type='WPA', password='SupperStrongPass:D'
)
qr_code.print_ascii()
qr_code.make_image().save('qr.png')
```

## Dépendances

-[Pillow](https://pypi.org/project/Pillow/)

- [qrcode](https://pypi.org/project/qrcode/)
