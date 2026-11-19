# Модель данных и AV-иерархия

## 1. Аватар

Аватар — цифровая копия физического объекта и контейнер состояния.

```json
{
  "avatar_id": "av-000001",
  "physical_object_ref": "building-001",
  "generation": 3,
  "graph_db_ref": "graph://avatar-000001",
  "avifc_ref": "avifc://avatar-000001@gen:3",
  "service_files": ["manifest.json", "index.json", "journal.ndjson"]
}
```

## 2. AV-иерархия

| Сущность | Код | Назначение |
|---|---|---|
| AVGALAXY | GAL | Глобальный контур, политики, маршруты |
| AVSTAR | STA | Домен, область ответственности |
| AVPLANET | PLA | Рабочий контур проекта |
| AVSPUTNIK | SPU | Подключаемый модуль знаний или правил |

Путь: `GAL.STA.PLA[.SPU]`.

## 3. Объекты планеты

- `build.plt` — строительный объект.
- `road.plt` — дорожный объект.
- `human.plt` — участник, роль, решение.
- `pla.pub` — публичная часть состояния.
- `pla.loc` — локальная часть состояния.

## 4. Сущность

```json
{
  "av_id": "wall-123",
  "av_type": "Wall",
  "path": "GAL01.STA03.PLA07",
  "generation": 3,
  "predecessor_ref": "wall-123@gen:2",
  "lifecycle_state": "active",
  "attributes": {},
  "relations": [],
  "provenance": {
    "source_ref": "ifc-003",
    "evidence_ids": [],
    "decision_id": null
  }
}
```

## 5. Связи

Базовые отношения:

- `REPRESENTED_ON`
- `DESCRIBED_BY`
- `MEASURED_BY`
- `COSTED_BY`
- `CALCULATED_BY`
- `SUBJECT_TO`

Каждая связь имеет независимые статусы:

- `review_status`: candidate / verified / rejected;
- `consistency_status`: unchecked / consistent / conflict;
- `freshness_status`: current / stale / unknown.
