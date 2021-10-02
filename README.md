Highlight IP
============

This extension will color any occurrences of IPv4 or IPv6 addresses.

![Screenshot](https://raw.githubusercontent.com/medo64/highlight-ip/main/images/screenshot.png)


## Extension Settings

This extension contributes the following settings:

* `highlight-ip.v4`: Determines if IPv4 addresses will be highlighted.

* `highlight-ip.v6`: Determines if IPv6 addresses will be highlighted.

* `highlight-ip.cidr`: Determines if subnet length (e.g. /24) will be
                       highlighted in addition to the address.

* `highlight-ip.strict`: Extra validation for proper formatting of IP address
                         (RFC5952 rules for IPv6) and subnet.


### Default Configuration

    "highlight-ip.v4": true,
    "highlight-ip.v6": true,
    "highlight-ip.cidr": true,
    "highlight-ip.strict": false,


## Extension Colors

This extension contributes the following colors:

* `ipaddress.network`: Color for IP address.

* `ipaddress.subnet`: Color for IP subnet length.

* `ipaddress.issue`: Color for the IP address breaking the rule.


### Default Colors

    "workbench.colorCustomizations": {
        "ipaddress.network": "textLink.foreground",
        "ipaddress.subnet": "textLink.foreground",
        "ipaddress.issue": "errorForeground",
    }


## Known Issues

### Not Coloring For Large Files

For performance reasons Visual Studio Code doesn't synchronize files that are
over 5MB in size (see [issue 27100](https://github.com/Microsoft/vscode/issues/27100)).
Therefore, no coloring will be done in large files. To avoid this you can set
`editor.largeFileOptimizations` to `false`.
