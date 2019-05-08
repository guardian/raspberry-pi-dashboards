

https://pimylifeup.com/raspberry-pi-kiosk/

The version of Chromium in Raspbian currently has uBlock Origin enabled -
this seems to block XHR requests like 
https://dashboard.ophan.co.uk/graph/pageviews/data , which means the graph
lines won't show.

Disable uBlock Origin to get the graph working again.