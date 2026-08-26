# BIM-to-Multi-Robot Task Graph

> A research prototype for compiling BIM/IFC and construction-process information into capability-aware, validated multi-robot task graphs, schedules, and execution evidence.

## 한국어 요약

BIM이나 디지털 시공계획을 로봇이 직접 이해할 수 있는 작업 단위, 선후관계, 공간 제약, 필요 능력, 성공조건으로 변환하고 여러 로봇에 배정하는 프로젝트입니다. 지상 건설에서 실행 가능한 핵심을 먼저 검증한 뒤, 통신지연·에너지·달 토양 등 달 건설 제약으로 확장합니다.

## Problem

BIM contains geometry and object semantics, while robot systems require explicit actions, capabilities, resources, zones, preconditions, effects, and completion evidence. The missing bridge is not only path planning. It is a traceable compiler and repair layer between changing construction intent and heterogeneous robot execution.

## Core pipeline

BIM/IFC + process plan -> semantic work items -> typed task graph -> capability matching -> constraint validation -> schedule/allocation -> dispatch interface -> execution evidence -> repair

## First prototype

- Python, JSON, and OR-Tools
- Synthetic BIM-like JSON before full IFC parsing
- Static compilation and scheduling before closed-loop replanning
- Lunar-specific vocabulary and constraints without pretending to have a lunar field validation
- Separate input, task-graph, and schedule artifacts

## Research contribution target

- Traceable transformation from source objects and work packages to robot tasks
- Typed dependencies with explicit preconditions and effects
- Capability-aware heterogeneous robot allocation
- Spatial, resource, energy, and exclusion-zone validation
- Completion-evidence contracts and execution-aware repair

## Current status

Research specification and phased prototype plan. Closed-loop multi-robot execution has not yet been demonstrated.

## Documents

- [ARCHITECTURE.md](ARCHITECTURE.md)
- [ROADMAP.md](ROADMAP.md)
- [EVALUATION.md](EVALUATION.md)
