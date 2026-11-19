# ArchiMate — контекст AVGALAXY (v0.1)

Слои упрощённо (витрина; не полный Tobit).

**Метрика успеха (одна):** площадь по норме проверена **без ручного пересчёта** — след: snapshot + criterion + finding + human decision.

```mermaid
flowchart TB
  subgraph actors [Business_Actors]
    Sponsor[Sponsor_or_Customer]
    Human[Human_decision_maker]
    BIMSpec[BIM_specialist]
  end
  subgraph value [Value]
    Report[Risk_and_compliance_report]
  end
  subgraph app [Application]
    Pilot[area_check_pilot]
    NormEng[Normative_engine]
    Mapping[Mapping_IFC_bSDD_glossary]
  end
  subgraph data [Data]
    Snapshot[Sealed_snapshot]
    Criterion[Norm_criterion]
    Finding[Finding]
    Decision[Decision]
  end
  Sponsor -->|"получает"| Report
  Report --> Decision
  Human -->|"единственный approve/reject"| Decision
  BIMSpec --> Pilot
  Pilot --> Snapshot
  Pilot --> Criterion
  Pilot --> Finding
  Finding --> Decision
  Mapping --> Pilot
  NormEng --> Criterion
```

**Читается за 30 сек:** пользователь/специалист гоняет пилот → finding → **человек решает** → спонсор получает отчёт о соответствии/риске.  
Finding без human decision не «закрыт». `geometry_basis` явен (не вид экрана).
