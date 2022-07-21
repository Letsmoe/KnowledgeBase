# Felder
Verbrauchsausweis:
- Anlass (enum<"Neubau", "Vermietung", "Verkauf", "Modernisierung", "Sonstiges">)
- Baujahr Heizung (int)
- Baujahr Gebäude (int)
- Anzahl Wohnungen (int)
- Saniert? (boolean)
- Straße (varchar)
- Hausnummer (int)
- PLZ (int)
- Ort (varchar)
- Wohnfläche (int)
- Keller (enum<"beheizt", "unbeheizt", "nicht">)
- Dachgeschoss (enum<"beheizt", "unbeheizt", "nicht">)
- Primärenergiequelle Start (timestamp)
- Brennstoff 1 (enum<...>)
- Einheit 1 (enum<...>)
- Verbrauch 1 (int)
- Verbrauch 2 (int)
- Verbrauch 3 (int)


# Funktionieren Nicht
- gckuid (Nur 6 mal benutzt, funktioniert nicht mehr richtig.) - ENTFERNT
- gcfiid (Nur 6 mal benutzt, funktioniert nicht mehr richtig.) - ENTFERNT
- AZusatzzeile (Wird nicht mehr ausgefüllt) - ENTFERNT
- ansprechpartnerklapper2 (Noch nie benutzt) - ENTFERNT
- anlagenkombi (Wird nicht mehr ausgefüllt) - ENTFERNT
- VermittlungHW (Wird nicht mehr ausgefüllt) - ENTFERNT
- nsumrechnungsfaktor2 (a.k.a. BRSUmrechnungsfaktor2 - SESSION wurde nicht mehr gefüllt) - ENTFERNT
- korrektur (Noch nie benutzt (Immer null)) - ENTFERNT

# Fragen
- bearbeitetkunde - Wird das noch benutzt?