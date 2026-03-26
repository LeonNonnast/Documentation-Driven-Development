# Documentation-Driven Development -- Manifest

## Die Grundidee

Jede Software löst ein Problem für jemanden. Bevor Code geschrieben wird, muss klar sein: für wen, und wie.

Documentation-Driven Development stellt die Dokumentation an den Anfang des Entwicklungsprozesses. Sie beschreibt das Produkt, bevor es gebaut wird -- aus der Perspektive derer, die es nutzen werden. Daraus werden technische Spezifikationen, Tests und schließlich Code abgeleitet.

Die Dokumentation ist kein Nebenprodukt der Entwicklung. Sie ist ihr Ausgangspunkt.

## Das Prinzip

**Schreibe die Dokumentation für Software, die noch nicht existiert.**

Beschreibe, was der Nutzer sieht. Was er klicken kann. Welche Meldungen erscheinen. Welche Fehler auftreten. Tue das in der Sprache des Nutzers, nicht in der Sprache des Entwicklers.

Code ist das Abbild der Dokumentation. Nicht umgekehrt.

## Wer ist "der Nutzer"?

Der Nutzer ist, wer das Produkt konsumiert. Das kann sein:

- **Ein Mensch**, der eine Oberfläche bedient
- **Ein Administrator**, der ein System konfiguriert
- **Ein Entwickler**, der eine API integriert
- **Ein KI-Agent**, der eine Schnittstelle aufruft

Die Perspektive ändert sich, das Prinzip bleibt: Erst beschreiben, was passiert. Dann bauen.

## Das Ebenen-Modell

```
  Dokumentation
  ├── Benutzerdokumentation       <- Was erlebt der Nutzer?
  └── Technische Dokumentation    <- Wie ist es gebaut?
              |
            Tests                 <- Der Beweis.
              |
            Code                  <- Die Realisierung.
```

### Benutzerdokumentation

Beschreibt das Produkt aus der Perspektive dessen, der es benutzt. Seiten, Abläufe, Meldungen, Fehler. In der Sprache des Nutzers. Dies ist der erste Schritt -- hier entsteht das Verständnis dafür, was gebaut werden soll.

### Technische Dokumentation

Wird aus der Benutzerdokumentation abgeleitet. Beschreibt Architektur, Komponenten, Schnittstellen, Datenmodelle, Entscheidungen. In der Sprache des Entwicklers. Richtet sich an alle, die das System bauen, warten oder erweitern.

### Tests

Stützen die Dokumentation. Sie beweisen, dass der Code sich so verhält, wie in Benutzer- und technischer Dokumentation beschrieben. Aus Abläufen werden E2E-Tests. Aus Fehlermeldungen werden Edge-Case-Tests. Aus Schnittstellenbeschreibungen werden Integrationstests.

### Code

Realisiert die Dokumentation. Er ist ihr Spiegelbild. Code verhält sich dokumentationskonform -- immer.

## Der Prozess

### Neues Feature

1. Benutzerdokumentation schreiben
2. Technische Dokumentation ableiten
3. Tests definieren
4. Implementieren

### Änderung am Verhalten

1. Benutzerdokumentation anpassen
2. Technische Dokumentation anpassen
3. Tests anpassen
4. Code anpassen

### Refactoring

1. Benutzerdokumentation bleibt unverändert -- das Nutzerverhalten ändert sich nicht
2. Technische Dokumentation anpassen -- neue Struktur, neues Pattern, neue Architekturentscheidung
3. Tests anpassen, falls sich technische Schnittstellen ändern
4. Code anpassen

### Entfernung

1. Dokumentation entfernen
2. Tests entfernen
3. Code entfernen

## Die Regel

> Wenn es nicht dokumentiert ist, existiert es nicht.
> Wenn es falsch dokumentiert ist, ist es fehlerhaft.
> Wenn es nicht mehr dokumentiert ist, wurde es entfernt.
>
> Code verhält sich dokumentationskonform.
> Wenn Dokumentation und Code nicht übereinstimmen, ist der Code falsch.

## Warum jetzt?

Documentation-Driven Development ist nicht neu. Die Idee existiert seit über einem Jahrzehnt. Was sich geändert hat, sind die Rahmenbedingungen:

- **KI kann Dokumentation als Kontext nutzen.** Eine präzise Beschreibung reicht, um funktionierenden Code zu generieren.
- **KI kann beim Schreiben der Dokumentation helfen.** Der Aufwand, der DDD bisher unwirtschaftlich machte, sinkt drastisch.
- **KI kann die Synchronisation sicherstellen.** Änderungen im Code können automatisch gegen die Dokumentation geprüft werden.

Das Argument "Dokumentation kostet zu viel Zeit" verliert seine Gültigkeit. Dokumentation wird zum effizientesten Weg, Software zu bauen.

## Was dieses Manifest nicht ist

- Kein starres Framework. Jedes Team adaptiert den Prozess.
- Kein Ersatz für agile Methoden. DDD ergänzt Scrum, Kanban und andere Vorgehensmodelle.
