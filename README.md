# Equity Screener snapshot mirror

The scan workflow in the private stock-screener repository overwrites the `latest` branch after every whole-market scan with the sanitized market snapshot: the SQLite database of scan results (gzip), the three map files, the peer medians and a `manifest.json`. The app's host fetches these files at boot over plain HTTPS, so it needs no token. Nothing here is user data; it is the same data the app shows to any visitor.
