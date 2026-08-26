# Roadmap

## Phase 0: Domain and benchmark selection

- Search for reusable public task graphs, PDDL domains, and assembly/construction benchmarks
- Define a small lunar construction scenario and a terrestrial analogue
- Freeze JSON schemas and validation rules

## Phase 1: Eight-week static compiler

### Weeks 1-2

- Create synthetic BIM-like input examples
- Define work items, robots, zones, dependencies, and evidence contracts
- Build schema validation and unit tests

### Weeks 3-4

- Implement deterministic rule-based task expansion
- Preserve source and revision traceability
- Reject missing or ambiguous required fields

### Weeks 5-6

- Implement capability matching and OR-Tools scheduling
- Add energy, resource, exclusion-zone, and precedence constraints

### Weeks 7-8

- Compare compiler output with manual reference graphs
- Run ablations and infeasibility tests
- Package reproducible examples and technical report

## Phase 2: IFC ingestion

- Add IfcOpenShell parsing
- Map selected IFC classes and property sets to work items
- Add 4D schedule or process-plan inputs

## Phase 3: Planning and simulation

- Connect symbolic planning and a simulated robot fleet
- Validate dispatch artifacts and completion evidence
- Distinguish local motion recovery from task-level repair

## Phase 4: Closed-loop repair

- Trigger repair from robot failure, site-state discrepancy, human intervention, or BIM revision
- Revalidate and dispatch revised assignment/schedule artifacts
- Measure stability and unnecessary plan churn

## Phase 5: Lunar constraints

- Add communication delay, charging and sunlight windows, regolith interactions, dust, thermal limits, and limited human intervention
- Compare performance with equivalent terrestrial scenarios
