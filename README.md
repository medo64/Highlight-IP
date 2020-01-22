Highlight IP
============

This extension will color any occurrences of IPv4 or IPv6 addresses.

![Screenshot](https://raw.githubusercontent.com/medo64/highlight-ip/master/images/screenshot.png)


## Extension Settings

This extension contributes the following settings:

* `highlight-ip.v4`: Determines if IPv4 addresses will be highlighted.

* `highlight-ip.v6`: Determines if IPv6 addresses will be highlighted.

Color is taken from `textLink.foreground` theme color.


### Default Configuration

    "highlight-ip.v4": true,
    "highlight-ip.v6": true


## Known Issues

### Not Coloring For Large Files

For performance reasons Visual Studio Code doesn't synchronize files that are
over 5MB in size (see [issue 27100](https://github.com/Microsoft/vscode/issues/27100)).
Therefore, no line-ending characters will be visible on large files. To avoid
this you can set `editor.largeFileOptimizations` to `false`.
