# PAF 4 — Vicensae System & Protocol

> **We do not store files; we encapsulate truth.**

## Vision

PAF 4 is a **Fiduciary Custody Regime**.

In this ecosystem, a work is not a fragmented asset stored in a third-party cloud. It is a **Vector Cinema** scene preserved inside a **High-Stability Judicial Container (HSJC)**.

Under the **VICENSÆ** protocol, the author’s declared intent remains **immutable, legible, verifiable, and sovereign** across time and platforms.

PAF 4 does not treat storage as the primary problem.  
It treats **custody, integrity, lineage, and rendering fidelity** as first-class concerns.

---

## Core Distinction: Regime vs Container

PAF 4 is built on a strict ontological distinction:

- **NotTR is the regime of access**  
  It governs identity, admission, and authorization.

- **HSJC is the container of truth**  
  It encapsulates the work as a self-describing, verifiable, renderable artifact.

This means:

- access is not custody,
- storage is not truth,
- visibility is not legitimacy.

The regime decides **who may enter**.  
The container defines **what it means to access the work legitimately**.

---

## System Architecture

The system is organized into independent modules with clear responsibilities.

### `/hsjc` — The Canonical Container
The ontological core of the system.

Responsibilities:
- manifest sealing,
- lineage declaration,
- rendering conditions,
- integrity metadata,
- deterministic packaging.

HSJC is the atomic unit of custody.  
Everything downstream operates on HSJC, never on raw files alone.

---

### `/ingest` — The Foundry
The first point of contact for incoming works.

Responsibilities:
- extract authorial intent,
- validate assets and metadata,
- normalize inputs,
- produce the canonical HSJC artifact.

**Contract:**  
`/ingest` never emits raw files downstream.  
Its only valid output is a sealed or sealable **HSJC**.

---

### `/vault` — The Sanctuary
Armored custody layer for canonical containers.

Responsibilities:
- persistent storage of HSJC artifacts,
- integrity preservation,
- redundancy and recovery support,
- protected custody boundaries.

The vault stores **containers**, not merely files.

---

### `/catalog` — The Ledger of Relations
Organizes discovery, indexing, and relationships across the collection.

Responsibilities:
- indexing,
- search metadata,
- work relationships,
- collection state projections.

**Important:**  
`/catalog` is **not** the source of truth.  
The source of truth is always the **HSJC** artifact.

---

### `/viewer` — The Projector
High-fidelity rendering engine.

Responsibilities:
- render directly from HSJC,
- respect rendering constraints,
- preserve authorial intent,
- avoid distraction or mutation.

**Rule:**  
The viewer does not interpret arbitrary storage objects.  
It renders only from valid HSJC specifications.

---

### `/auth` — The NotTR Regime
Identity, admission, and governance layer.

Responsibilities:
- identity validation,
- admission control,
- access policy enforcement,
- governance integration (RAGO / Poimandres).

This layer protects entry.  
It does not replace semantic custody.

---

### `/api` — The Neural Link
Secure communication language between modules.

Responsibilities:
- authenticated inter-module communication,
- transport of requests and verification results,
- protocol-safe exposure of system capabilities.

---

## Axial Principles

### 1. Work First
The system must sustain the work’s magic, not obscure it.

### 2. Fiduciary Sovereignty
Control belongs to the author.  
Infrastructure acts only as custodian, never as sovereign owner.

### 3. Regime Before Exposure
No work appears in raw form without passing through the proper custody and admission boundaries.

### 4. Truth Must Be Encapsulated
A work must not depend on a fragile URL, an opaque viewer state, or an undocumented storage backend.  
Truth must travel inside a verifiable container.

### 5. Rendering Fidelity
The work must be presented as declared, without arbitrary distortion, silent mutation, or platform noise.

### 6. Determinism
HSJC must be reproducible and content-addressed whenever applicable.  
Equivalent inputs should produce equivalent canonical outputs under the same rules.

### 7. Independent Verification
Any authorized node should be able to verify an HSJC artifact independently.

### 8. Tending the Garden
> *“Flowers do not ask for permission to bloom, but someone must tend the garden for it to endure.”*

---

## Operational Principles

### Canonical Flow

```text
raw assets + author metadata
        ↓
      /ingest
        ↓
       HSJC
        ↓
      /vault
        ↓
     /catalog
        ↓
      /viewer