# UnityAI V2

> **An autonomous AI development agent for Unity**

UnityAI V2 ist ein KI-gestützter Entwicklungsagent für den Unity Editor. Das System kombiniert Codegenerierung, automatisierte Reparatur, Unity-Editor-Automatisierung, Runtime-Validierung und strukturierte Entwicklungsplanung zu einem vollständig orchestrierten Workflow.

---

# Vision

UnityAI V2 verfolgt das Ziel, nicht nur Quellcode zu generieren, sondern komplette Entwicklungsaufgaben innerhalb eines Unity-Projekts autonom zu planen, auszuführen, zu validieren und bei Fehlern selbstständig zu reparieren.

Der Agent kann dabei sowohl C#-Code erzeugen als auch Änderungen direkt im Unity-Projekt durchführen.

---

# Architektur

```text
                        User Prompt
                             │
                             ▼
                  Development Planner
                             │
          ┌──────────────────┴──────────────────┐
          │                                     │
          ▼                                     ▼
    Patch Pipeline                      Tool Pipeline
          │                                     │
          ▼                                     ▼
    Compile & Repair                   Unity Editor Tools
          │                                     │
          └──────────────────┬──────────────────┘
                             ▼
                    Runtime Validation
                             │
                             ▼
                      Automatic Repair
```

---

# Erreichte Milestones

## ✅ Milestone 1 – AI Foundation

- KI-Integration in den Unity Editor
- Prompt-Verarbeitung
- Codegenerierung
- Editor-UI

---

## ✅ Milestone 2 – Development Planning

- Development Plan Sessions
- Schrittbasierte Planung
- Plan Lifecycle
- Statusverwaltung
- Entwicklungsplan-Orchestrierung

---

## ✅ Milestone 3 – Patch Pipeline

- Patch-Generierung
- Patch Preview
- Patch Apply
- Automatische Kompilierung
- Fehlerbehandlung

Pipeline:

```text
Plan
→ Patch Generation
→ Patch Apply
→ Compile
```

---

## ✅ Milestone 4 – Autonomous Code Agent

- automatische Compile-Erkennung
- Compile Watcher
- Repair-Pipeline
- automatische Patch-Reparatur
- erneute Kompilierung
- automatische Fortsetzung des Plans
- Repair-Limit
- korrekte Trennung von:
  - Step Compilation
  - Validation Compilation

Pipeline:

```text
Plan
→ Patch
→ Apply
→ Compile
→ Repair
→ Repair Apply
→ Compile
→ Continue
```

---

## ✅ Milestone 5 – Workflow Refactoring

Die Workflow-Logik wurde vollständig von der UI getrennt.

Neue Komponenten:

- PatchCoordinator
- RepairCoordinator
- PatchApplyCoordinator

Die Editor-Fenster dienen heute hauptsächlich als Benutzeroberfläche.

---

## ✅ Milestone 6 – Approval & Safety

- Approval Policy
- kontrollierte Patch-Anwendung
- Risiko-Klassifizierung
- sichere autonome Ausführung

---

## ✅ Milestone 7 – Testing Infrastructure

- Headless End-to-End Tests
- EditMode Tests
- Workflow Tests
- Compile Tests
- Repair Tests
- Statusübergangs-Tests

---

## ✅ Milestone 8 – Generic Tool Framework

Ein vollständig generisches Tool-System.

Bestehend aus:

- Tool Registry
- Tool Planner
- Tool Coordinator
- Tool Executor
- Tool Execution Context
- Tool Result References

Architektur:

```text
Planner
→ Tool Plan
→ Validator
→ Coordinator
→ Executor
→ Result
```

---

## ✅ Milestone 9 – Tool Plan Validation

Regelbasierte Validierung mit u. a.:

- unbekannte Tools
- doppelte Result IDs
- Referenzprüfung
- Typprüfung
- Argumentvalidierung
- Risiko-Regeln
- Modus-Regeln
- Tool-Limits

---

## ✅ Milestone 10 – Scene Tools

Unterstützt u. a.:

- CreateGameObject
- AddComponent
- SaveScene
- Objekt-Hierarchien
- Komponentenverwaltung

---

## ✅ Milestone 11 – Serialized Property Tools

Unterstützt:

- int
- float
- bool
- string
- Vector-Typen
- Color
- Enum
- Unity Object References

inklusive Typvalidierung und Fehlerbehandlung.

---

## ✅ Milestone 12 – Tool End-to-End Tests

Umfassende Testabdeckung für:

- vollständige Tool-Pläne
- Fehlerfälle
- Rollback
- Idempotenz
- Referenzprüfung
- Property-Validierung
- Save/Dirty-State

---

## ✅ Milestone 13 – Prefab Tools

Unterstützt:

- Prefab erstellen
- Prefab laden
- bearbeiten
- speichern
- entladen
- instanziieren
- validieren

---

## ✅ Milestone 14 – Stable Unity References

- GlobalObjectId
- GUID-basierte Referenzen
- stabile Objektidentifikation
- Referenzen über mehrere Ausführungsschritte hinweg

---

## ✅ Milestone 15 – Asset Transactions

- Asset-Backups
- Rollback
- Commit
- Wiederherstellung
- temporäre Arbeitsbereiche

---

## ✅ Milestone 16 – Structured Post Validation

Validierung nach jeder Tool-Ausführung.

Unter anderem:

- GameObjects
- Komponenten
- Prefabs
- Assets
- Szenen
- Property-Werte

---

## ✅ Milestone 17 – Runtime / PlayMode Tools

Unterstützt:

- PlayMode starten
- PlayMode stoppen
- Runtime-Objekte prüfen
- Runtime-Komponenten validieren
- Exceptions überwachen
- PlayMode Assertions

---

## ✅ Milestone 18 – Automatic Tool Repair

Automatische Analyse fehlgeschlagener Tool-Pläne.

Unterstützt:

- Repair Plans
- Replanning
- erneute Ausführung
- erneute Validierung
- Repair-Limits

---

## ✅ Milestone 19 – Hybrid AI Agent

UnityAI V2 kombiniert inzwischen mehrere Entwicklungsbereiche in einem einzigen Workflow.

```text
Development Plan

├── Code Generation
├── Patch Pipeline
├── Unity Tool Pipeline
├── Compile Pipeline
├── Runtime Validation
└── Automatic Repair
```

Dadurch kann der Agent:

- C#-Code erzeugen
- Code kompilieren
- Compile-Fehler reparieren
- Unity-Szenen bearbeiten
- Prefabs erstellen
- Komponenten konfigurieren
- Referenzen setzen
- Assets verwalten
- Runtime validieren
- Fehler automatisch replannen

---

# Aktueller Entwicklungsstand

UnityAI V2 verfügt derzeit über:

- ✅ Entwicklungsplanung
- ✅ Patch-Generierung
- ✅ Autonome Code-Reparatur
- ✅ Tool-Framework
- ✅ Tool-Planung
- ✅ Tool-Validierung
- ✅ Szenenbearbeitung
- ✅ Prefab-Workflow
- ✅ Asset-Transaktionen
- ✅ Runtime-Tools
- ✅ Strukturierte Post-Validation
- ✅ Automatische Tool-Reparatur
- ✅ End-to-End-Testabdeckung

---

# Langfristige Vision

UnityAI V2 soll sich zu einem vollständigen KI-Entwicklungsagenten entwickeln, der unterschiedliche Spezialisierungen kombinieren kann.

Geplante Erweiterungen umfassen beispielsweise:

- Blender-Integration
- Git-Integration
- Build-Automatisierung
- Asset-Generierung
- Multi-Tool-Orchestrierung
- Erweiterte Runtime-Analyse

Dadurch soll UnityAI V2 nicht nur Code schreiben, sondern komplette Entwicklungsprozesse innerhalb und außerhalb des Unity Editors autonom durchführen können.

---

# Lizenz

Dieses Projekt befindet sich aktiv in der Entwicklung. API-Strukturen und interne Komponenten können sich zwischen Versionen ändern.
