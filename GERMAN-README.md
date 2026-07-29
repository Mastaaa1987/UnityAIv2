# Deutsch Fassung:

# Pre Prompt

Man glaubt es kaum Ich habe heute in den Selben Prompt über dem Ich einen Planungsauftrag an meine LLM übergebe eingegeben:

```
Rigge das vorhandene Modell
Assets/UnityAI/Generated/Models/MeinModel.glb
mit Blender als Generic-Rig.

Erzeuge eine loopende Idle-Animation namens Idle und speichere das
riggte Modell als
Assets/UnityAI/Generated/Models/MeinModel_Rigged.fbx.

Importiere das FBX anschließend in Unity, konfiguriere es als Generic Rig,
analysiere das Skeleton, erstelle In-Place- und Root-Motion-Clips,
validiere die Animation und erzeuge einen Animator Controller unter
Assets/UnityAI/Generated/Animations/MeinModel.controller.

Erstelle abschließend ein Prefab unter
Assets/UnityAI/Generated/Prefabs/MeinModel.prefab.
```

Und die LLM hat mir diesen Plan entworfen:

```
- Erstellt den vertraglichen Rahmen für das Rigging: Generic-Rig, Name 'MeinModel', Höhe standardmäßig 1.7m, Animation 'Idle' als loopende Animation.
- GeneratePrefab=true für spätere Prefab-Erstellung.
- Nutzt Blender, um das bestehende GLB-Modell (Assets/UnityAI/Generated/Models/MeinModel.glb) als Generic-Rig zu riggen und eine loopende Idle-Animation zu erstellen.
- Ausgabe als FBX unter Assets/UnityAI/Generated/Models/MeinModel_Rigged.fbx.
- Importiert das geriggte FBX (Assets/UnityAI/Generated/Models/MeinModel_Rigged.fbx) in Unity und konfiguriert es als Generic Rig. Importiert Animationen.
- Analysiert das Skeleton des importierten Modells, erstellt In-Place- und Root-Motion-Clips für die Idle-Animation und validiert die Animation.
- Erstellt einen Animator Controller mit der Idle-Animation (In-Place-Variante) als Standard-State unter Assets/UnityAI/Generated/Animations/MeinModel.controller.
- Erstellt ein Prefab aus dem importierten, riggten Modell mit dem Animator Controller unter Assets/UnityAI/Generated/Prefabs/MeinModel.prefab.
```

Und er hat den Plan erfolgreich ausgeführt! 

Das glb Model habe Ich zuvor mit ComfyUI in einer Prompt to Image to 3D Model in 30 min generieren lassen. die LLM hat mir jetzt daraus eine fxb MOdel mit Rig 

Bones & Idle Animation gemacht und das ganze nur mit den möglichen Tools die ich hier über UnityAIv2 freigegeben habe xD !!!

UnityAI ist nun in der Lage ganze Kampfsysteme zu schreiben, Models zu erstellen, zu Animieren, zu importieren. Das ganze im Game modus auf Komplie fehler zu 

untersuchen und zu korrigieren! Und das beste dabei ist das die LLM komplett austauschbar ist, ob nun ChatGPT, OpenAI, oder lokale quen3.5 modelle (oder deepseek 

usw.) via Ollama oder LM Studio, spielt keine rolle die LLM braucht nicht zu wissen wie Unity, Blender, oder ComfyUI funktioniert ! 

Viel zu kross ganz ehrlich!

# UnityAI V2

> **An autonomous AI development agent for Unity**

UnityAI V2 ist ein KI-gestützter Entwicklungsagent für den Unity Editor. Das System kombiniert Codegenerierung, automatisierte Reparatur, Unity-Editor-Automatisierung, Runtime-Validierung und strukturierte Entwicklungsplanung zu einem vollständig orchestrierten Workflow.
Der gesamte Prozess wird von einem LLM meiner Wahl angetrieben – von Mistral.ai über OpenAI bis hin zu vollständig lokal gehosteten Modellen wie Qwen 3.5 oder DeepSeek, bereitgestellt über Ollama oder LM Studio. Sämtliche Schritte, von der Erstellung eines Entwicklungsplans bis zur Generierung von C#-Code im Rahmen eines Patch-Zyklus, können lokal ausgeführt werden, wodurch zusätzliche Kosten für cloudbasierte KI-Dienste entfallen.

---

# Vorab

Vorab für jeden der sich fragt warum nur leere Files existieren? Ich habe Files in einem Privaten Repo gehostet. Für jeden der wirklich an diesem Projekt interessiert ist, der kann ja mal versuchen via Telegram nett danach zu fragen, nichts ist unmöglich insofern auch vorkenntnisse mitgebracht werden. Aber wichtig ist: User freundlicher Chat, ein einfaches Hi führt zum direkten Bann.

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

