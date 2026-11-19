# Lieferando-Klon

## Idee
Kleine Restaurants in der Umgebung von Lieferando abwerben und jedem eine eigene Bestell-App bauen.
Nutzen für das Restaurant: Lieferando-Provision entfällt (ca. 14 % pro Bestellung zzgl. MwSt.).

## Struktur
- Hauptverzeichnis: gemeinsame Grundlagen des Klons (Architektur, Features, Entscheidungen).
- Pro Kunde (Restaurant) ein eigenes Unterverzeichnis, z. B. `kunden/<restaurant-name>/`.
- Erst Grundlagen hier klären, dann pro Kunde herunterbrechen.

## Arbeitsweise
- Notizen und Entscheidungen hier im Hauptverzeichnis festhalten.
- Kundenspezifisches (Menü, Branding, Lieferzonen, Konditionen) nur im jeweiligen Unterverzeichnis.

## Apple / App Store (geprüft gegen App-Store-Richtlinien)
- Digitale Güter/Features in der App: In-App-Kauf Pflicht (3.1.1), Apple-Provision 30 %, 15 % mit Small Business Program (< 1 Mio. $ Umsatz).
- Physische Waren/Leistungen außerhalb der App (Essen): In-App-Kauf nicht zu verwenden, stattdessen Apple Pay, Karte, Zahlungsanbieter (Stripe, Adyen, Mollie, PayPal) (3.1.3(e)). Keine Apple-Provision (folgt daraus, steht nicht wörtlich dort).
- Regel 4.2.6: Template-/Baukasten-Apps werden abgelehnt, wenn wir sie im Namen der Restaurants einreichen. Erlaubte Wege:
  1. Jedes Restaurant reicht seine App selbst ein (eigener Developer-Account, 99 $/Jahr).
  2. Eine Sammel-App für alle Restaurants ("picker"-Modell, Apple nennt "restaurant finder"). Nachteil: kein eigenes Branding, wir werden quasi ein kleines Lieferando.
- Alternative: Web-App (PWA) pro Restaurant, ohne App Store. Nachteil: weniger Sichtbarkeit, eingeschränkte Push-Nachrichten auf dem iPhone.
- Google Play: ähnliche Logik (nicht gegen die Richtlinien geprüft).

## Zahlung / Recht (nicht geprüft)
- Geld sollte direkt zum Restaurant fließen (z. B. Stripe Connect). Läuft es über uns, ist evtl. eine Zahlungsdienst-Erlaubnis (ZAG/BaFin) nötig: Anwalt klären.
- Gebühren der Zahlungsanbieter (grob 1,5 % + 0,25 € Karte, ca. 3 % PayPal) noch prüfen.
- Barzahlung bei Lieferung als Option.

## Risiko
- Lieferando bringt auch Kunden/Reichweite. Ohne eigenen Kundenstrom sinken die Bestellungen. Marketing-Konzept für Restaurants nötig.

## Offen
- Technischer Stack, Zahlungsabwicklung, Lieferlogik, Hosting, eigene Marge/Preismodell: noch nicht entschieden.
