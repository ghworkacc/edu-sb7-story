# Story Brief Contract

Load this reference after domain evidence has been normalized and the activation gate in the parent skill passes.

## Input Packet

```yaml
audience:
  type: customer | internal | public
  roles: []
artifact:
  type: markdown | powerpoint | word | visual | video
  purpose: inform | decide | align | celebrate
desired_action: ""
evidence:
  - id: source-1
    claim: ""
    source: ""
    confidence: confirmed | user-provided | hypothesis
    sensitivity: internal | customer-safe | public-safe
constraints: []
```

## Audience Modes

| Mode | Story subject | Guide | Primary action |
|---|---|---|---|
| `customer-facing` | Customer, customer team, or customer persona | Joint team, Microsoft, partner, or platform | Mutually agreed customer next step |
| `internal-decision` | Customer remains the subject; internal team is the acting audience | Account team and operating model | Decision with owner and date |
| `internal-celebration` | Customer journey and achieved outcome | Cross-role team | Replicable lesson or next growth motion |
| `public-safe` | Approved customer or anonymized persona | Publicly supportable capabilities | Low-risk public action |

## Seven Beats

1. **Hero**: who is trying to make progress, and toward what outcome?
2. **Problem**: what external obstacle blocks progress? Add internal tension or stakes only when grounded.
3. **Guide**: how does the enabling team or system show empathy and competence without taking over?
4. **Plan**: what two or three concrete steps reduce ambiguity?
5. **Action**: what one next decision or behavior is required, by whom?
6. **Failure avoided**: what evidenced risk, cost, delay, or friction is reduced?
7. **Success**: what customer-centered future state becomes possible?

These are composition checks, not mandatory artifact headings.

## Artifact Patterns

| Need | Pattern |
|---|---|
| Executive brief | Outcome -> current tension -> guided plan -> decision -> evidence |
| Transformation deck | Current state -> stakes -> three-step path -> proof -> future state -> action |
| Technical-to-business report | Business outcome -> uncertainty -> proof plan -> decision evidence -> handoff |
| Internal decision brief | Customer outcome -> execution gap -> options -> recommendation -> owner/date |
| Win story | Customer challenge -> team strategy -> outcome -> reusable lesson -> next motion |
| Video or visual | Challenge -> guided movement -> visible success -> action |

## Output Schema

```yaml
mode: customer-facing
audience: []
hero: { entity: "", desired_outcome: "" }
problem: { external: "", internal: "", stakes: "" }
guide: { empathy: "", competence_evidence: [] }
plan: []
action: { next_step: "", owner: "", due_date: null }
failure_avoided: ""
success: { future_state: "", metrics: [] }
evidence_refs: []
assumptions: []
gaps: []
confidentiality: internal
artifact_outline: []
```

## Quality Gate

- Headline describes progress or a literal decision, not a product capability.
- Problem precedes solution.
- Guide supports rather than displaces the hero.
- Plan has no more than three primary steps.
- One next action is visible.
- Success is a better state, not deployment.
- Every metric, quote, motive, and risk is sourced or labeled.
- Product and architecture details remain supporting evidence.