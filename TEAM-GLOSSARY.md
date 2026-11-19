# Язык команды (ops)

Не путать с продуктовым словарём: [12-GLOSSARY.md](12-GLOSSARY.md).  
Здесь — как мы **говорим между собой и с разработчиками**. Одно понятие — одно слово.

| Термин | По-человечески | Как сказать разработу |
|---|---|---|
| **Канон** | Единственное место правды о продукте | Source of truth = git `main`, не Drive и не чат |
| **Витрина** | Public репо для спонсора/гранта | Showcase repo (`AVGALAXY`) |
| **Кухня / VIP** | Private: пилоты, Excel, сырьё | Kitchen / private (`AVGALAXY-VIP`) |
| **Drive** | Доска и дневники, не продукт | Coordination only |
| **Daily-context** | Срез дня: сделано / открыто / next | Handoff note, не лог сессии |
| **Очередь / TASKS** | Работы с ID и владельцем | Backlog tickets |
| **Human decision** | Только человек закрывает finding | No auto-approve; `pending_human` |
| **Finding** | Результат проверки правила | Ещё не решение |
| **Decision** | OK / reject человека | Закрывает finding |
| **Snapshot** | Замороженный вход проверки | Immutable input |
| **geometry_basis** | Явный базис геометрии (напр. net finish) | Не «как на экране» |
| **G0 / G1…** | Ступени упаковки к гранту | Milestone витрины, не semver продукта |

**Правило:** новый термин — только если кто-то уже переспросил. Синонимы запрещены.
