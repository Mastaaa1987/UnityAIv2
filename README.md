# Pre Prompt

It’s hard to believe—today I entered the following prompt to pass a planning task to my LLM:

```
Rig the existing model
Assets/UnityAI/Generated/Models/MeinModel.glb
using Blender as a Generic Rig.

Create a looping idle animation named 'Idle' and save the
rigged model as
Assets/UnityAI/Generated/Models/MeinModel_Rigged.fbx.

Then, import the FBX into Unity, configure it as a Generic Rig,
analyze the skeleton, create in-place and root-motion clips,
validate the animation, and generate an Animator Controller at
Assets/UnityAI/Generated/Animations/MeinModel.controller.

Finally, create a prefab at
Assets/UnityAI/Generated/Prefabs/MeinModel.prefab.
```

And the LLM devised this plan for me:

```
- Establishes the specifications for rigging: Generic Rig, name 'MeinModel', default height 1.7m, 'Idle' animation as a looping animation.
- GeneratePrefab=true for subsequent prefab creation.
- Uses Blender to rig the existing GLB model (Assets/UnityAI/Generated/Models/MeinModel.glb) as a Generic Rig and create a looping idle animation.
- Outputs as FBX at Assets/UnityAI/Generated/Models/MeinModel_Rigged.fbx.
- Imports the rigged FBX (Assets/UnityAI/Generated/Models/MeinModel_Rigged.fbx) into Unity and configures it as a Generic Rig. Imports animations.
- Analyzes the imported model's skeleton, creates in-place and root-motion clips for the idle animation, and validates the animation.
- Creates an Animator Controller with the idle animation (in-place variant) as the default state at Assets/UnityAI/Generated/Animations/MeinModel.controller.
``` - Creates a prefab from the imported, rigged model with the Animator Controller at `Assets/UnityAI/Generated/Prefabs/MeinModel.prefab`.
```

And it successfully executed the plan!

I previously used ComfyUI to generate the GLB model—going from prompt to image to 3D model—in just 30 minutes. The LLM then turned that into an FBX model with a rig,

bones, and an idle animation—and it did all of this using only the tools I enabled here via UnityAIv2 xD!!!

UnityAI is now capable of writing entire combat systems, as well as creating, animating, and importing models. It can even check for and fix compilation errors while in Play Mode!

And the best part is that the LLM is completely interchangeable—whether it's ChatGPT, OpenAI, or local Qwen 3.5 models (or DeepSeek, etc.) via Ollama or LM Studio,

it doesn't matter; the LLM doesn't need to know how Unity, Blender, or ComfyUI actually work!

Honestly, it's just mind-blowing!

# UnityAI V2

For German Readme look at GERMAN-README.md ...

> **An autonomous AI development agent for Unity**

UnityAI V2 is an AI-powered development agent for the Unity Editor. The system combines code generation, automated repair, Unity Editor automation, runtime validation, and structured development planning into a fully orchestrated workflow.
The entire process is powered by an LLM of your choice—ranging from Mistral.ai and OpenAI to fully locally hosted models like Qwen 3.5 or DeepSeek, served via Ollama or LM Studio. Everything from creating a development plan to generating C# code via a patch cycle can be handled locally, eliminating the additional costs associated with cloud-based AI services.

---

# In advance

For anyone wondering why there are only empty files: I’ve hosted the actual files in a private repository. If you’re genuinely interested in the project, feel free to try asking nicely via Telegram—nothing is impossible, provided you have some prior knowledge. But one important thing: keep the chat friendly—a simple "Hi" will get you banned immediately.

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

