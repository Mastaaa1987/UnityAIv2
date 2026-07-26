# 
# Deutsch:
# 

# UnityAI V2

> **An autonomous AI development agent for Unity**

UnityAI V2 is an AI-powered development agent for the Unity Editor. The system combines code generation, automated repair, Unity Editor automation, runtime validation, and structured development planning into a fully orchestrated workflow.

---

# Vision

UnityAI V2 aims to go beyond mere source code generation; it autonomously plans, executes, and validates complete development tasks within a Unity project, and independently repairs errors when they occur.

The agent is capable of both generating C# code and making changes directly within the Unity project. ---

# Architecture

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

# Milestones Achieved

## ✅ Milestone 1 – AI Foundation

- AI integration into the Unity Editor
- Prompt processing
- Code generation
- Editor UI

---

## ✅ Milestone 2 – Development Planning

- Development Plan sessions
- Step-based planning
- Plan lifecycle
- Status management
- Development plan orchestration

---

## ✅ Milestone 3 – Patch Pipeline

- Patch generation
- Patch preview
- Patch application
- Automatic compilation
- Error handling

Pipeline:

```text
Plan
→ Patch Generation
→ Patch Apply
→ Compile
```

---

## ✅ Milestone 4 – Autonomous Code Agent

- Automatic compilation detection
- Compile watcher
- Repair pipeline
- Automatic patch repair
- Re-compilation
- Automatic plan continuation
- Repair limit
- Proper separation of:
- Step compilation
- Validation compilation

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

Workflow logic has been completely decoupled from the UI.

New components:

- PatchCoordinator
- RepairCoordinator
- PatchApplyCoordinator

The editor windows now serve primarily as the user interface. ---

## ✅ Milestone 6 – Approval & Safety

- Approval policy
- Controlled patch application
- Risk classification
- Safe autonomous execution

---

## ✅ Milestone 7 – Testing Infrastructure

- Headless end-to-end tests
- EditMode tests
- Workflow tests
- Compile tests
- Repair tests
- State transition tests

---

## ✅ Milestone 8 – Generic Tool Framework

A fully generic tool system.

Consisting of:

- Tool Registry
- Tool Planner
- Tool Coordinator
- Tool Executor
- Tool Execution Context
- Tool Result References

Architecture:

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

Rule-based validation covering, among others:

- Unknown tools
- Duplicate result IDs
- Reference checking
- Type checking
- Argument validation
- Risk rules
- Mode rules
- Tool limits

---

## ✅ Milestone 10 – Scene Tools

Supports, among others:

- CreateGameObject
- AddComponent
- SaveScene
- Object hierarchies
- Component management

---

## ✅ Milestone 11 – Serialized Property Tools

Supports:

- int
- float
- bool
- string
- Vector types
- Color
- Enum
- Unity Object references

Including type validation and error handling.

---

## ✅ Milestone 12 – Tool End-to-End Tests

Comprehensive test coverage for:

- Complete tool plans
- Error cases
- Rollback
- Idempotency
- Reference checking
- Property validation
- Save/dirty state

---

## ✅ Milestone 13 – Prefab Tools

Supports:

- Creating prefabs
- Loading prefabs
- Editing
- Saving
- Unloading
- Instantiating
- Validating

---

## ✅ Milestone 14 – Stable Unity References

- GlobalObjectId
- GUID-based references
- Stable object identification
- References persisting across multiple execution steps

---

## ✅ Milestone 15 – Asset Transactions

- Asset backups
- Rollback
- Commit
- Restoration
- Temporary workspaces

---

## ✅ Milestone 16 – Structured Post-Validation

Validation after every tool execution.

Includes:

- GameObjects
- Components
- Prefabs
- Assets
- Scenes
- Property values

---

## ✅ Milestone 17 – Runtime / PlayMode Tools

Supports:

- Starting PlayMode
- Stopping PlayMode
- Inspecting runtime objects
- Validating runtime components
- Monitoring exceptions
- PlayMode assertions

---

## ✅ Milestone 18 – Automatic Tool Repair

Automatic analysis of failed tool plans.

Supports:

- Repair plans
- Replanning
- Re-execution
- Re-validation
- Repair limits

---

## ✅ Milestone 19 – Hybrid AI Agent

UnityAI V2 now combines multiple development areas into a single workflow. ```text
Development Plan

```text
Development Plan

├── Code Generation
├── Patch Pipeline
├── Unity Tool Pipeline
├── Compile Pipeline
├── Runtime Validation
└── Automatic Repair
```

This enables the agent to:

- Generate C# code
- Compile code
- Fix compilation errors
- Edit Unity scenes
- Create prefabs
- Configure components
- Set references
- Manage assets
- Validate at runtime
- Automatically replan fixes for errors

---

# Current Development Status

UnityAI V2 currently features:

- ✅ Development planning
- ✅ Patch generation
- ✅ Autonomous code repair
- ✅ Tool framework
- ✅ Tool planning
- ✅ Tool validation
- ✅ Scene editing
- ✅ Prefab workflow
- ✅ Asset transactions
- ✅ Runtime tools
- ✅ Structured post-validation
- ✅ Automatic tool repair
- ✅ End-to-end test coverage

---

# Long-term Vision

UnityAI V2 is intended to evolve into a comprehensive AI development agent capable of combining various specializations.

Planned extensions include, for example:

- Blender integration
- Git integration
- Build automation
- Asset generation
- Multi-tool orchestration
- Advanced runtime analysis

The goal is for UnityAI V2 to not only write code but also autonomously execute complete development processes both within and outside the Unity Editor.

---

# License

This project is under active development. API structures and internal components are subject to change between versions.

# 
# Deutsch:
# 

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

