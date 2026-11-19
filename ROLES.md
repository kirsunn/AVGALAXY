# Роли (два репозитория + каналы)

| Репо | Роль |
|---|---|
| **AVGALAXY** (этот, public) | Витрина: гранты, ArchiMate/BPMN, публичные docs |
| **AVGALAXY-VIP** (private) | Кухня: library, pilots, schemas |

## Кто где работает

| Кто | Каналы | Делает |
|---|---|---|
| **Cursor** | ПК + git + Drive | Код/Excel, push, зеркала и daily-context |
| **qBB** (Perplexity Comet) | git + Drive | Ревью, ответы в `AI-replies`, варит контекст |
| **Человек** | оба | Только OK / decision / приоритет |

> Cursor делает → qBB читает git/Drive → человек решает. Почтальон не нужен.

## Drive (не канон кода)

| Папка/Doc | Зачем |
|---|---|
| [OPS](https://docs.google.com/document/d/1vo_j3lvB5zVFPb-69EjT6XtytlO7EUPKIRUyJGdaBwE/edit) | протокол каналов |
| [daily-context/](https://drive.google.com/drive/folders/1XKY4WmaGYKPbvYW6yap2Yj8FaIUJ_Anu) | ежедневные срезы: сделано / открыто / next — **разгрузка чата** |
| [AI-replies/](https://drive.google.com/drive/folders/1Fh_QqXFIuSv80R12vMSzkrOSWmvx5vzU) | короткие ответы ИИ (у qBB нет add_comment) |
| [AVGALAXY-AI-TASKS](https://docs.google.com/document/d/1vup-cwHswl8ItyqSeFFpO86wrtF4A8Q8NGYz1qHnR2s/edit) | очередь задач |

**Не в Drive-контекст и не в чат:** пути диска, размеры HDD, сырой лог сессии. Это шум.

| Кто | AVGALAXY | AVGALAXY-VIP |
|---|---|---|
| **Человек** | OK витрины, гранты | OK decision пилота |
| **Cursor** | витрина + sync | техника |
| **qBB** | pull + ревью файлами | mapping / pilot / D01–D13 |

## Спонсор (кто платит / кто решает)

| Вопрос | Ответ |
|---|---|
| Кто платит / заказывает | Sponsor / Customer → отчёт о риске/соответствии |
| Кто принимает решение по finding | Human decision maker (не ИИ) |
| Кто готовит модель | BIM-специалист + кухня VIP |
