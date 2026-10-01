# YouTubeJH Verbindung

Dieses Repository liefert signierte Remote-Konfigurationen für YouTubeJH.

## Update-Sicherheit V4.1

- `manifest.json` wird vom eingebetteten Root-Key `root-2026` signiert.
- Das Manifest autorisiert getrennte Runtime-Schlüssel über `trustedKeys`.
- `update-main-2026` ist der bevorzugte Runtime-Schlüssel.
- `update-emergency-2026` ist der vorbereitete Notfall-/Fallback-Schlüssel.
- `keysetRevision` verhindert ein Zurückrollen auf eine ältere Schlüsselliste.
- `disabledKeyIds` kann kompromittierte Runtime-Schlüssel dauerhaft sperren.
- `validFrom` / `validUntil` begrenzen die Gültigkeit jedes Schlüssels.
- Runtime-Envelopes tragen `keyId`, damit der Loader direkt den richtigen Schlüssel prüft.
- SHA-256-Fingerprints und Prüfzeit werden vom Loader für die Diagnose gespeichert.
- Stable und Beta liegen als unveränderliche Revisionen unter `runtime/stable/` und `runtime/beta/`.

Private Schlüssel gehören niemals in dieses Repository.
