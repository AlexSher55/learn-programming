# Модуль 5 — Rules и AGENTS.md

Rules — постоянные инструкции агенту (стиль, ограничения, «как у нас принято»).

## Типы

| Тип | Где |
|-----|-----|
| Project rules | `.cursor/rules/*.mdc` |
| User rules | настройки Cursor (на все проекты) |
| Team rules | Teams / Enterprise |
| AGENTS.md | обычный markdown в корне (и вложенных папках) |

## Как применяются project rules

- **Always Apply** — в каждый чат
- **Apply Intelligently** — по `description`
- **Specific Files** — по `globs`
- **Manual** — через `@имя-правила`

Файлы должны быть `.mdc` с frontmatter. Обычный `.md` в `.cursor/rules` игнорируется.

Приоритет: Team → Project → User.  
Держи правила короткими и actionable (&lt; ~500 строк).

Документация: [Rules](https://cursor.com/docs/rules)

## AGENTS.md

Простой способ зафиксировать: как запускать проект, как тестировать, чего не делать.  
В этом репозитории уже есть корневой `AGENTS.md`.

## Memories (важно)

Старые «IDE Memories» в UI убрали — для постоянных предпочтений используй **Rules / AGENTS.md**.  
Отдельно существуют Memories у **Automations** (облако) — это другая история.

## Упражнения

1. Прочитай корневой `AGENTS.md` и попроси агента следовать ему в следующем ответе.
2. Создай `.cursor/rules/learning.mdc` с Always Apply: «объясняй кратко, после теории давай упражнения».
3. Создай правило с glob только для `practice/**` (например: «всегда комментируй неочевидные места»).

## Готово, когда

Знаешь разницу User vs Project rules и умеешь создать `.mdc`.
