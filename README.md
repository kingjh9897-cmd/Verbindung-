# Verbindung-

Remote-Konfiguration für YouTubeJH.

## Update-System v4

- `manifest.json` ist ein signiertes, atomares Envelope und zeigt auf unveränderliche Runtime-Revisionen.
- `runtime/stable/rev-*.json` enthält getestete Stable-Runtimes.
- `runtime/beta/rev-*.json` enthält Beta-Runtimes.
- Jede Runtime ist selbst signiert; zusätzlich prüft der Loader die SHA-256-Prüfsumme aus dem Manifest.
- Der Loader behält die letzte funktionierende Runtime und kann bei wiederholten instabilen Starts automatisch zurückrollen.
- `minLoaderVersion` verhindert inkompatible Runtime-Updates.
- Vertrauenswürdige zusätzliche Public Keys können über ein bereits gültig signiertes Manifest eingeführt werden.

Die alten `runtime.json`, `runtime.sig.hex`, `config.json` und `config.sig` bleiben vorerst nur für ältere Loader erhalten.
