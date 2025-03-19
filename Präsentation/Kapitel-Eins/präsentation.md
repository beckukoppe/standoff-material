---
marp: true
theme: gaia
class: titel
---
<!-- _class: lead -->
<!-- _theme: default -->

# LLM-gesteuerte Agenten in Computerspielen

`Kapitel Eins`

---
<!-- _class: lead -->

Von **Cedric Beck** und **Felix Koppe**

---

## Agenda

- Einleitung
- Spielidee
- Moodboards
- Architektur
- Herausforderungen
- Technik
- Ausblick

---

## Einleitung

- Zuversichtlich, dass **Echtzeitinteraktion** möglich ist

- Hardware wahrscheinlich als begrenzender Faktor

---

## Spielidee: Kernaspekte

-  Die Möglichkeiten von LLMs ausschöpfen
    - Dynamische Reaktionen auf das Verhalten des Spielers
    - Breit gefächerte Geschichte mit **minimalen Einschränkungen**
    - Sprache muss zentrale Rolle spielen

- Den Spieler durch Entscheidungsdruck und Zeitlimitationen fordern
    - Fokus auf Immersion und eine intensive Erfahrung
    - Der Spieler spricht

---

## Spielidee: "Standoff"

- Der Spieler spielt den Kriesenmanager während einer Geiselnahme
    - Er verhandelt mit den Geiselnehmern per **Funk** oder **Telefon**
    - Maßnahmen führen zur Konfliktlösung oder Eskalation

- Der Spieler muss sich entscheiden was er wann macht

- Dem Spieler stehen Live-Überwachungsbilder zur Verfügung

---

## Spielidee: Potenzielle Features

- Der Spieler muss eine **Pressekonferenz** halten
    - Reporter stellen kritische Fragen zum Krisenmanagement
    - Nachrichtenkanal überträgt die Konferenz in Echtzeit
    - Das Verhältniss zu den Geiselnahmen wird durch die Aussagen des Spielers beeinflusst

- **Polizeidatenbank** durchsuchen (gefüllt mit hilfreichen und irrelevanten Datensätzen)
- Telefonate (mit Informanten oder Polizeipräsident)
- Kollegen benötigen Anweisungen
- Der Spieler kann erreichen, dass die Geiselnehmer ihn persönlich empfangen

---

## Spielidee: Schauplatz

- Fiktive Stadt (erzählerische Freiheiten)
- Freistehendes Gebaude (**Bank** oder **Supermarkt**)
- Von Polizei Abgesperrt, Schaulustige und **Reporter**
- **Mobile Einsatztzentrale** als "Büro" des Spielers

---

## Moodboards: Zentrale

![w:500 h:520](moodboard_zentrale.png)

---

## Moodboards: Pressekonferenz

![w:500 h:520](moodboard_pressekonferenz.png)

---

## Architektur

- Layer Ansatz
    - **Mehrere Modelle**
    - Ein großes Hauptmodell
    - Mehrere kleinere spezialisierte Modelle

- Neustarts kleinerer Modelle um Halluzinationen zu vermeiden

---

## Architektur

- **GAMEMASTER** LLM:
    - Größeres Modell
    - Hält die Geschichte erzählerisch beisammen
    - Schreibt anweisungen für die untergeordneten Modelle

- **SLAVE** LLMs:
    - Kleineres modell
    - Verkörpern Personen in Dialogen (Reporter/Geiselnehmer/usw.)
    - hält sich an anweisungen vom GAMEMASTER
    - gibt gezielt Informationen preis oder oder hält sie zurück

---

## Herausforderungen

- Echtzeitverarbeitung und Reaktionsgeschwindigkeit
- Mehrere modelle
    - Koordination
    - Ressourcen

- Kontrolle der Geschichte
    - Initiale Prompts müssen präzise sein
    - Darstellung muss zu Geschichte passen

---

## Technik: Allgemein

- Sollte Open Source sein

---

## Technik: Backends

- llamacpp
- ollama

---

## Technik: Text2Speech und Speech2Text

- **Text2Speech**
- piper
- OpenVoiceV2

- **Speech2Text**
- Whisper (openai)

---

## Technik: Modelle

- Flexibel austauschbar

- Wichtige Aspekte
    - Geschwindigkeit
    - Rollenspiel Fähigkeiten

- Mögliche Modelle:
    - mixtral
    - deepseek-r1

---
<!-- _class: lead -->

## Ausblick

dies und das
dies und jenes
bla bla bla
