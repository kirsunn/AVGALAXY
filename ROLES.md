# Роли (два репозитория)

| Репо | Роль |
|---|---|
| **AVGALAXY** (этот, public) | Витрина: гранты, ArchiMate/BPMN, публичные docs |
| **AVGALAXY-VIP** (private) | Кухня: library, pilots, schemas, session-notes |

> Cursor делает → проверяющий ИИ (qBB) читает git → человек решает.

**Почтальон не нужен:** задания для проверяющего — в [TASKS.md](TASKS.md). Человек только OK/decision.

| Кто | AVGALAXY | AVGALAXY-VIP |
|---|---|---|
| **Человек** | OK витрины, гранты, «кто платит» | OK decision пилота |
| **Cursor** | правки витрины + пишет TASKS | техника, XLSX |
| **Проверяющий ИИ** | pull + TASKS + ревью | mapping / pilot / D01–D13 |
| **Drive** | только канал | только канал |
