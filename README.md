# 🐸 Plugin-Frosch

Ein spezialisierter Chat-Assistent für **Java- und Minecraft-Plugin-Entwicklung**
(Spigot / Paper / Bukkit / Folia / Forge / Fabric), der direkt im Browser läuft
und die [Claude API](https://console.anthropic.com) von Anthropic nutzt.

![Status](https://img.shields.io/badge/status-aktiv-4c9a5c)
![Sprache](https://img.shields.io/badge/sprache-Deutsch-orange)

## Live-Demo

👉 `https://DEINNAME.github.io/plugin-frosch/`
*(Link anpassen, sobald GitHub Pages aktiv ist)*

## Was ist das?

Plugin-Frosch ist eine einzelne HTML-Datei mit eingebautem Chat-Interface. Es ist
kein eigenes KI-Modell, sondern Claude mit einem fest eingestellten System-Prompt,
der ihn auf Minecraft-Plugin-Code fokussiert:

- Moderner, sauberer Java-Code (Java 17+)
- Best Practices für Bukkit/Paper: korrekte Event-Listener, Async-Handling,
  `NamespacedKey`s, passende `plugin.yml`-Einträge
- Vollständige, direkt einsetzbare Code-Blöcke inklusive Imports
- Antworten auf Deutsch (Englisch wird automatisch erkannt)

## Nutzung

1. Seite öffnen (lokal per Doppelklick auf `index.html` oder über die Live-Demo).
2. Eigenen Anthropic-API-Key eingeben (kostenlos erstellbar unter
   [console.anthropic.com](https://console.anthropic.com) → **API Keys**).
3. Loslegen – z. B. mit:
   - „Erstelle einen `/heal`-Command mit Cooldown und Permission"
   - „Warum wirft mein Listener eine NullPointerException?"
   - „Baue ein einfaches Kit-System mit YAML-Config"

## Wichtiger Hinweis zum API-Key

Der Key wird **nur im Arbeitsspeicher deines Browser-Tabs** gehalten, nirgendwo
gespeichert oder übertragen außer direkt an `api.anthropic.com`. Er verschwindet
beim Neuladen der Seite.

⚠️ **Trage niemals deinen echten API-Key fest in den Code ein und lade die Datei
so hoch.** Jeder, der die Seite dann öffnet, könnte deinen Key mitlesen und auf
deine Kosten Anfragen stellen. Die Eingabe im Browser ist genau deshalb so gebaut.

Kosten entstehen nur nutzungsbasiert direkt bei Anthropic (in der Regel wenige
Cent pro Anfrage) – dieses Repo selbst verlangt nichts.

## Lokal ausführen

Kein Build-Prozess nötig – einfach `index.html` im Browser öffnen.

```bash
git clone https://github.com/DEINNAME/plugin-frosch.git
cd plugin-frosch
# index.html im Browser öffnen
```

## Selbst hosten (GitHub Pages)

1. Repo-Einstellungen → **Settings → Pages**
2. **Source**: `Deploy from a branch`
3. **Branch**: `main`, Ordner `/ (root)`
4. Speichern – nach ca. 1 Minute ist die Seite live

## Anpassen

Der System-Prompt liegt direkt in `index.html` in der Variable `SYSTEM_PROMPT`
und lässt sich beliebig umschreiben, z. B. um auf eine bestimmte Minecraft-Version
oder einen anderen Plugin-Stil zu fokussieren.

## Lizenz

Nutzung auf eigenes Risiko. Kein offizielles Anthropic-Produkt.
