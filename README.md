# KI-Angebots-Check für Freelancer

Kostenlose, datensparsame Werkzeuge für klarere Freelancer-Angebote – plus eine öffentliche Red-Team-Review, die ohne Vorkasse automatisch geliefert wird.

[10-Punkte-Check starten](https://n5rjgsqj5g-cmd.github.io/sers-money-router-live/ki-angebots-check.html) · [Praxisguide lesen](https://n5rjgsqj5g-cmd.github.io/sers-money-router-live/guides/angebot-klar-formulieren-mit-ki/) · [Zweitmeinung anfragen](https://n5rjgsqj5g-cmd.github.io/sers-money-router-live/services/angebot-red-team/)

## Was sofort nutzbar ist

- **Interaktiver Angebots-Score:** zehn Felder für Zielgruppe, Problem, Ergebnis, Zeit, Ablauf, Preis, Beleg, Grenzen, CTA und risikoarmen Einstieg.
- **Offline-Kit:** Workbook, sieben faktenbasierte Copy-Prompts, Scorecard und 30-Minuten-Plan als offene HTML-, Markdown- und CSV-Dateien.
- **Praxisguide:** Vorher-nachher-Beispiel, sicherer KI-Workflow, Datenschutz-Minimum und Qualitätsprüfung.
- **Öffentliche Red-Team-Review:** bereinigten Text als Issue einreichen und eine strukturierte Prüfung direkt als Kommentar erhalten.

[Kit als ZIP laden](https://n5rjgsqj5g-cmd.github.io/sers-money-router-live/downloads/ki-angebots-check-v1.0.0.zip) · [Release und Prüfsumme](https://github.com/n5rjgsqj5g-cmd/sers-money-router-live/releases/tag/v1.0.0)

## Die Review wird wirklich geliefert

Die Workflow-Automation reagiert auf neue Issues mit dem Präfix `[Angebots-Review]` und veröffentlicht:

1. einen reproduzierbaren 10-Felder-Score,
2. die stärksten Engpässe oder einen ehrlichen 20/20-Hinweis,
3. eine Kernfassung ausschließlich aus eingereichten Fakten,
4. fünf skeptische Kundenfragen,
5. einen kleinen nächsten Test.

Untrusted Issue-Inhalte werden auf Prompt-Injection geprüft. Bei einem Modell- oder API-Ausfall liefert eine getestete deterministische Regelprüfung weiterhin das vollständige Basisergebnis. Das Workflow-Token erhält nur `contents: read`, `issues: write` und `models: read`.

- [Live-Demo: unscharfes Angebot, 7/20](https://github.com/n5rjgsqj5g-cmd/sers-money-router-live/issues/2)
- [Live-Demo: vollständiges Angebot, 20/20](https://github.com/n5rjgsqj5g-cmd/sers-money-router-live/issues/1)
- [Automatischer Lieferlauf](https://github.com/n5rjgsqj5g-cmd/sers-money-router-live/actions/workflows/offer-review.yml)

## Fairer Zahlungsweg

Alle Downloads sind ohne Anmeldung kostenlos. Die öffentliche Review verlangt keine Vorkasse. Erst wenn ein Ergebnis konkret hilft, wird freiwilliger PayPal-Support angeboten:

- 9 € für das kostenlose Toolkit
- 19 € nach einer gelieferten öffentlichen Review

Eine Zahlung kauft keine Priorisierung und ist keine steuerlich absetzbare Spende. Es gibt keine Auftrags- oder Umsatzgarantie.

## Datenschutz und Grenzen

Der Browser-Score lädt keine Analyse- oder Tracking-Skripte und sendet keine Antworten an einen Server. GitHub-Issues sind dagegen **öffentlich**: niemals Namen, Kontakt- oder Kundendaten, Zugangsdaten, interne Zahlen, Vertragsinhalte oder andere vertrauliche Informationen einreichen.

Die Materialien prüfen Angebotskommunikation und Positionierung. Sie sind keine Rechts-, Steuer-, Vertrags- oder Umsatzberatung.

## Entwicklung und Tests

Die Review-Logik läuft ohne zusätzliche npm-Abhängigkeiten:

```bash
node --test tests/offer-review.test.mjs
```

Die Tests decken Issue-Parsing, Scoring, vollständige und lückenhafte Angebote, Prompt-Injection, Secret-Leaks, Modellantwort und sicheren Fallback ab.
