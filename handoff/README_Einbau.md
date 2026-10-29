# SANNIS Produktseite 179 · Variante C (neues Design) · Einbau

Stand 29.10.2026 · Quelle: SANNIS Style Guide 2026, Kapitel 14 „eShop“. Ansprechpartner: Manuel Kössler (SANNIS Marketing).

## Was das ist
Ein fertiger `wp:html`-Block (Markup + CSS + kleines Skript) für die WooCommerce-Produktseite **Bio-Leinöl extra nativ 500 ml (Produkt-ID 179)**.
Er ersetzt die bisherige Beschreibung durch die neue Gliederung (Größenwahl 250/500 ml, Vorteile unter dem Button, Pillen-Tabs,
Statement-Band, Zahlen-Kacheln, Abschnitte mit Bild, sechs Anwendungen, Hinweis „Nie erhitzen“, FAQ, Sticky-Kaufleiste mobil).
Nur Optik-Schicht: **kein Eingriff in Warenkorb, Checkout, Plugins oder Theme.** Der Kauf-Button bleibt das Woo-Original,
die Sticky-Leiste scrollt nur dorthin (kein click/submit).

## Dateien
| Datei | Zweck |
|---|---|
| `SANNIS_Produktseite_179_VarianteC_Block.html` | Der Block, komplett kopierbar (ca. 33 KB) |
| `assets/fonts/` | Schriften: ITC Avant Garde Gothic Pro Bold + Book als WOFF2 (Original, Lizenz SANNIS, nur für sannis.at); Hanken Grotesk (SIL OFL) für Fließtext |
| `assets/img/s_pattern_tile_tonintone.png` | S-Pattern-Kachel für das Statement-Band |

## Einbau (ca. 20 Minuten)
1. **Assets hochladen:** Ordner `assets/` so auf den Server legen, dass die Dateien unter `https://sannis.at/wp-content/uploads/sannis-brand/fonts/…` und `https://sannis.at/wp-content/uploads/sannis-brand/img/…` erreichbar sind
   (z. B. per FTP nach `wp-content/uploads/sannis-brand/`). Anderer Pfad? Dann im Block alle `https://sannis.at/wp-content/uploads/sannis-brand` ersetzen.
2. **Sicherung:** Im Produkt 179 die aktuelle Beschreibung (Code-Editor, Cmd+A/Cmd+C) als Datei sichern.
3. **Einfügen:** Produkt 179 → Beschreibung → Code-Editor. Der Block **„Kundenstimmen“ (`#kundenstimmen`) bleibt unverändert davor**;
   den Inhalt der Datei dahinter einfügen (ein `wp:html`-Block). Keine Zeile aus dem Block weglassen, keine `on…`-Attribute ergänzen.
4. **Cache:** WP Rocket Cache leeren („Delay JavaScript“ bleibt aktiv, der Block ist darauf ausgelegt).
5. **Prüfen (mobil zuerst):** iPhone 393 px ohne Überbreite, Größenwahl 250/500 ml, Sticky-Leiste erscheint nach dem Kaufbereich,
   Tabs „Zutaten & Nährwerte“ und „Produktsicherheit“ gestaltet, Warenkorb-Button unverändert. Dann Desktop.
6. **Preis 250 ml:** steht fest im Block (17,90 €) → bei Preisänderung dort nachziehen. Der 500-ml-Preis wird live aus der Seite gelesen.

## Schrift
Headlines = **ITC Avant Garde Gothic Pro** (Original, SANNIS hat die Lizenz gekauft, Freigabe für Headlines 29.10.2026). Die WOFF2-Dateien Bold und Book
liegen in `assets/fonts/` und sind im Block per `@font-face` („SANNIS Display“) eingebunden. Nur auf SANNIS-Domains einsetzen, nicht weitergeben.
Weitere Schnitte (Extra Light, Medium, Demi, Obliques) liegen bei SANNIS (Drive „Logos & Branding/Schriften_ITC_Avant_Garde_Gothic_Pro_gekauft_2026“).

## Regeln
- Firewall-sicher: kein HTML in JS-Strings, keine `on…`-Attribute, keine externen Skripte, kein Base64.
- Rollout auf die anderen Leinöle erst nach Messung der Abschlussrate auf 179 (Block als synchronisiertes Muster wie die Kundenstimmen).
- Variante B (aktueller Shop-Stil, ohne neue Schrift) liegt als Alternative im Projekt (`02_varianten/block_B.html`).
