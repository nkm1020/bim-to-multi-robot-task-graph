# Evaluation Plan

## Compiler correctness

- Schema-valid output rate
- Source and revision traceability coverage
- Precision/recall of required tasks and dependencies against expert references
- Precondition/effect and resource-constraint correctness
- Deterministic reproducibility

## Scheduling and allocation

- Feasible-schedule rate
- Makespan, energy, idle time, and resource conflict count
- Capability mismatch count
- Solver runtime and optimality gap
- Robustness to duration and energy uncertainty

## Baselines

1. Manual expert graph and schedule
2. Simple rule-based compiler without capability reasoning
3. Capability-aware compiler without optimization
4. Full constraint-based compiler and scheduler

Use reusable public graphs or PDDL domains where suitable before inventing a manual baseline from scratch.

## Repair evaluation

- Recovery success after failure or site revision
- Time to produce and validate a revised plan
- Number of reassigned tasks and changed dependencies
- Schedule stability and unnecessary churn
- Constraint violations before and after repair
- Percentage of revised plans actually dispatched in simulation

## Experimental scenarios

- Missing robot capability
- Robot failure during a critical task
- Resource or zone conflict
- Delayed material availability
- BIM/work-package revision
- Communication or energy restriction

## Reporting boundary

Do not label path rerouting as task replanning. Do not claim lunar validation from synthetic lunar constraints. Publish schemas, seeds, solver settings, failure cases, and raw evaluation artifacts.
