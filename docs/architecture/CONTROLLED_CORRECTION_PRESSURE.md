# Controlled Correction-Pressure Path

The CORE architecture separates the generation of conversational responses from the process of system correction and improvement. This document describes the "Controlled Correction-Pressure" path, an optional architectural layer designed to allow the system to benefit from reviewed corrections without compromising system stability or enabling autonomous mutation.

## Architectural Separation

The system separates responsibilities across several distinct layers to maintain strict safety boundaries:

- **Durable Reviewed-Correction Storage**: A dedicated vault layer persists corrections that have been manually reviewed and verified. This layer does not store raw failed outputs as future pressure.
- **Relevance/Topology-Based Selection**: A selection layer identifies candidate reviewed records from durable storage that are most relevant to the current interaction state. This layer acts as a filter, not as the storage authority.
- **Runtime Admission Control**: An admission gate evaluates selected candidates to determine if they are eligible to become runtime context. Rejected or below-threshold candidates are discarded.
- **Optional Runtime Consumption**: The core interaction runtime can optionally consume admitted records as correction pressure. 

## Safety Boundaries

The following non-negotiable safety boundaries define the correction-pressure path:

1. **No Automatic Promotion**: Failed outputs are never automatically promoted into the system's runtime behavior or memory.
2. **No Raw Failure Usage**: Raw failed response text is never used as runtime pressure.
3. **Opt-In Behavior**: The correction-pressure provider is optional. Default system behavior remains unchanged unless the provider is explicitly configured.
4. **Admission Gating**: Selected records must pass a rigorous admission gate before they are permitted to influence the runtime context.
5. **Auditability**: The entire path is auditable. The system records counts and high-level decisions (considered, selected, admitted, rejected) without exposing private payloads.

## Verification Posture

This architecture ensures that correction pressure remains bounded, auditable, and subject to human-led review. By separating storage, selection, and admission from the primary runtime, CORE prevents uncontrolled memory mutation and maintains its commitment to deterministic, evidence-oriented engineering.
