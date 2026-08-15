# NAMHunt Beta-Manifest

Zwei statische Dateien. Sie steuern, wann die NAMHunt-Beta endet.

- `beta.json` — Enddatum, Mindest-Build-ID, widerrufene Builds, Hinweistext
- `beta.json.sig` — Signatur ueber die **Rohbytes** von `beta.json`

Aendern: Wert in `beta.json` setzen, dann

    BetaManifestSign sign beta.json ~/.namhunt/beta_private.key

und beide Dateien committen. Der private Schluessel gehoert NICHT hierher.

Das Manifest kann das Beta-Ende nur **vorziehen**, niemals hinausschieben.
Hintergrund: `AUFTRAG_BETA_GATE.md` / `BEFUND_BETA_GATE.md` im Hauptprojekt.
