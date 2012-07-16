Files over clouds
===

API
---
This is the mothership, it hold the data and talks to the differents sub projects.  
The API handle:
- user managment, auth creation grant
- authorisation
- routing of the file accros the different piers
- social feed
- subscriptions for the scraper, and later for notifications
- whish list
- download basket

Pier
----
The pier act as a proxy for accesseing and manipulating files. Because of it is not part of the API is can run on any other machin and is flexible enough for any crazy setup.
The pier does of could do:
- talk and auth itself on a single mothership API
- file download with http-range
- token based auth with the mothership API
- proxy communication to a transmission daemon
- unrar on the fly
- zip/tar on the fly


Scraper
-------
The scraper goes on website and grab data/file to feed the mothership API with. The mothership API provides list of wanted subscriptions or whised files.
The scraper sends whater he find that match back to the API.

CLI Client
----------
To be determined

Web Client
----------
To be determined, but mostly a 1 to 1 mapping of all the features of the API.

Streamer
--------
Big R&D subject, how and what can we bring to the tablets, iPad and Nexus 7 and to the html5 video tag.  
This could lead to pure awesomeness, but todisapointment, worse scenario VLC web plugin.


Sub projects hosted on github
- https://github.com/3on/foc-api
- https://github.com/3on/foc-scraper
- https://github.com/3on/foc-pier
- cli client
- web client
- streamer