# Architecture

## 1. Versioned inputs

### Construction model

- Elements and geometry/work zones
- Work packages and quantities
- Construction method and sequence constraints
- Revision and source identifiers

### Robot catalog

- Capabilities and payload
- Tools and material compatibility
- Mobility and reach
- Energy and communication constraints
- Safety and environmental limits

### Site state

- Available resources
- Exclusion zones and access routes
- Human interventions
- Observed completion and failure events

## 2. Compiler stages

1. Extract semantic work items
2. Expand each work item into typed executable tasks
3. Generate preconditions, effects, dependencies, resources, and success evidence
4. Match capability-qualified robot candidates
5. Validate spatial, temporal, resource, and safety constraints
6. Optimize assignment and schedule
7. Emit task graph, schedule, and validation artifacts

## 3. Task schema

Each task should include:

- id, type, source object, and revision
- action, target, quantity, zone, and pose requirements
- required capabilities, tools, materials, and resources
- preconditions, effects, dependencies, and mutex constraints
- duration and energy estimates
- uncertainty and allowed recovery behavior
- completion evidence and acceptance rule

## 4. Layered execution path

The long-term architecture may connect:

- Custom BIM/process semantic extractor and compiler
- PlanSys2 for symbolic planning and repair
- Open-RMF for heterogeneous fleet and resource coordination
- Vendor or VDA 5050 adapters
- BehaviorTree.CPP for local recovery
- MoveIt Task Constructor for manipulation planning

These are candidate integration layers, not implemented dependencies in the first prototype.

## 5. Replanning taxonomy

- Path rerouting: changes motion path only
- Local correction: changes pose or control behavior
- Task reassignment: changes responsible robot
- Schedule repair: changes dependency-aware timing or work sequence

A system is called task-level replanning only when a live trigger produces, validates, and dispatches a revised plan artifact.
