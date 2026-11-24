# Learning log

One entry per week, written during the Saturday retro (15 minutes). The most recent entry goes at the top.
Reviewers and the committee read this file to see which week you're on.

## Template

## Semana 01 · 2026-11-23 · Scalability vs. Elasticity

**What I learned:**
- **Scalability is structure** (it *can* grow). **Elasticity is speed and reversibility** (it grows *in time* and gives back what it no longer needs). Elasticity depends on scalability.
- **Auto scaling ≠ elasticity.** In-memory state cancels it out.
- **The bottleneck moves to the least elastic component.** If a component can't be scaled (the payment gateway), decouple it or apply admission control.
- **Payments queue:** `backlog = (inflow − outflow) × peak duration`. Always do the math.

**What I struggled with:**
-

**What I applied at work:**
-

**Review findings and what I fixed:**
- I mixed up the two terms. Fix: mnemonic, *the spring is elasticity, the ground is scalability.*

**Confidence by topic (1 to 5):**
- Scalability vs. elasticity: 4
- Auto scaling and state: 3
- Bottlenecks and admission control: 5
- Queue backlog math: 2

**Actual hours:** 2

---

<!-- Las entradas empiezan aquí -->
