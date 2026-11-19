# BPMN 2.0 — контур нормативной проверки (v0)

Процесс пилота area-check (упрощённо).

```mermaid
flowchart LR
  start([Start]) --> ingest[Ingest_or_surrogate_model]
  ingest --> basis[Set_geometry_basis]
  basis --> snap[Seal_snapshot]
  snap --> run[Evaluate_criterion]
  run --> find[Emit_finding]
  find --> human{Human_decision}
  human -->|approve| done([Accepted])
  human -->|reject| revise[Revise_model_or_rule]
  revise --> snap
  done --> finish([End])
```

**События:** snapshot immutable; смена отделки → новый snapshot, не правка старого.  
**Gateway:** только человек меняет `decision.status` с `pending_human`.
