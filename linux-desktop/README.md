# Linux Desktop

This image is a Ubuntu desktop, exposed using Kasm VNC.

Kasm includes a html5 client, for easy access. It's configured to listen on port 6443.

## Known issues

When running the virtual desktop in an iframe, there is a issue updating the resolution to match the iframe size. To work around that, add the following query parameter to the url: `show_control_bar=true`. This will make it match the iframe size, and respond to resize events.
