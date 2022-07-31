# Änderungen
### [[2022-07-27]]
In den Skripten `ausweispdfkern.php`, `empfehlungenneu.php`, `datenblatt.php` und `datenblattneu.php` wurde `empfehlungenneu.php` inkludiert, dieses exportierte mehrere Variablen die für die Erstellung von Empfehlungen gedacht waren, diese konnten allerdings zu einem [[Array]] zusammengefasst werden.

### [[2022-07-27]]
Im Skript `ausweisnwpdf.php` werden Variablen aus dem `empfehlungenneu.php` Skript benutzt, allerdings wird dieses niemals inkludiert, wie konnte das jemals funktionieren?