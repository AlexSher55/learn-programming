# Модуль 9 — Skills, Hooks, Plugins, Subagents

## Skills

Пакет `SKILL.md` — переиспользуемый playbook.  
Вызов: `/имя` или авто по `description`.

Где лежат: `.cursor/skills/`, user skills, и др.  
Встроенные примеры: `/create-rule`, `/create-skill`, `/create-hook`, `/review`, …

Документация: [Skills](https://cursor.com/docs/skills)

## Hooks

Скрипты вокруг цикла агента (`hooks.json`):  
формат после правки, блок опасных shell-команд, аудит MCP и т.д.

Документация: [Hooks](https://cursor.com/docs/hooks)

## Plugins и Commands

Plugin = бандл rules + skills + MCP + hooks + commands.  
Commands = готовые `/`-промпты (markdown-воркфлоу).

## Subagents

Отдельные агенты с изолированным контекстом (explore, shell, browser; можно свои в `.cursor/agents/`).  
Skills — для одноразовых сценариев; subagents — для параллельной/изолированной работы.

Документация: [Subagents](https://cursor.com/docs/subagents)

## Упражнения

1. `/create-skill` — skill «объясни тему курса коротко + дай 2 упражнения».
2. Вызови свой skill через `/`.
3. (Опционально) Проектный hook `afterFileEdit`, который логирует или форматирует файл.

## Готово, когда

Отличаешь rule (постоянные нормы) от skill (сценарий по запросу) и hook (автоматика вокруг агента).
