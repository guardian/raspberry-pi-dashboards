# Raspberry Pi Dashboards

There are a few of these around the office - a Raspberry Pi hooked up to a spare monitor, 
showing useful information to the team, but there can be a few hiccups getting them going,
here's a guide you might find useful.

## Setting up the Raspbian operating system

### Getting on to the network

### Clock time!

Raspberry Pi computers don't come with a battery-backed clock, so when they turn on they
have no idea what the time is - they have to connect to an [NTP server](https://en.wikipedia.org/wiki/Network_Time_Protocol)
in order to find out what the time is. Here in the Guardian offices, we've mysteriously
seen Raspberry Pi devices fail to do this - because of network or firewall reasons? -
and so they don't know the correct time, and when they try to visit HTTPS pages
they declare the certificate invalid because it seems to have been signed in the future!

One way of getting round this problem is to add a [battery-packed clock](https://shop.pimoroni.com/products/adafruit-pirtc-pcf8523-real-time-clock-for-raspberry-pi)
to the Raspberry Pi. We've done this successfully on the Data Technology team, there's a small
bit of configuration to get it working but after that it's one less thing to worry about!

## Setting up Chromium in kiosk mode
