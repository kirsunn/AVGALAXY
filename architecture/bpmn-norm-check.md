# BPMN 2.0 — контур нормативной проверки (v0.1)

**Метрика успеха:** площадь проверена без ручного пересчёта (след в finding + decision).

```mermaid
flowchart TB
  start([Start]) --> ingest[Ingest_or_surrogate_model]
  ingest --> basis[Set_geometry_basis]
  basis --> snap[Seal_snapshot]
  snap --> run[Evaluate_criterion]
  run --> find[Emit_finding]
  find --> human{{HUMAN_DECISION}}
  human -->|approve| done([Accepted_rebirth_ok])
  human -->|reject| revise[Revise_model_or_rule]
  revise --> snap
  done --> finish([End])
```

**Стоп-точка за 30 сек:** жирный шлюз `HUMAN_DECISION` — единственный путь к Accept. До него нет rebirth/accept.

**События:** snapshot immutable; смена отделки → новый snapshot.  
**Gateway:** только человек меняет `decision.status` с `pending_human`.
