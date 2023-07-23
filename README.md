# WIFI QRCODE UTILITY

A simple perl script to generate QR Code for joining a wifi network

![QR Code](./example.png)

## Usage

```Shell
# Barcode with red color
wifi_qrcode.pl --color="#AA0000" mynetwork mypassword

# Larger dotsize without a password
wifi_qrcode.pl --margin=5 --dotsize=4 mynetwork

# Larger dotsize, best error correction
wifi_qrcode --dotsize=5 --correction=Q mynetwork mypassword
```

## Options

- **--filename** default wifi-barcode.png
- **--ssid**
- **--password**
- **--authtype** WPA or WEP, default WPA
- **--hidden** SSID Hidden, default false
- **--bgcolor** Background color of image, default transparent for PNG, white otherwise
- **--color** Foreground color of image, default black
- **--margin** Margin size for image
- **--dotsize** Dotsize for qr code
- **--correction** Error correction level. Valid values are M, L, H or Q

## Uses libqrencode

```Shell
# Install on MacOS
brew install qrencode
```

## Perl Dependencies

Requires
[Getopt::Long](https://metacpan.org/pod/Getopt::Long),
[Imager::File](https://metacpan.org/pod/Imager::File),
[Imager::File::PNG](https://metacpan.org/pod/Imager::File::PNG),
[Imager::QRCode](https://metacpan.org/pod/Imager::QRCode),
[Pod::Usage](https://metacpan.org/pod/Pod::Usage)

```Shell
# Install with Carton
carton

# Install with cpanm
cpanm --installdeps .

# Install with cpan
cpan Getopt::Long Imager::File Imager::File::PNG Imager::QRCode Pod::Usage
```

