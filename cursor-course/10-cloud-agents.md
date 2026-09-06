# Модуль 10 — Cloud Agents и Automations

## Cloud Agents

Агент на удалённой VM: можно параллелить задачи, ноутбук может спать.  
Раньше назывались Background Agents.

Доступ: Desktop «Cloud», [cursor.com/agents](https://cursor.com/agents), Slack/GitHub/`@cursor`, API.

Обычно нужны: подключённый Git-хостинг + подходящий план.  
Критично настроить environment (зависимости, секреты, сеть).

Документация: [Cloud Agents](https://cursor.com/docs/cloud-agent) · [Best practices](https://cursor.com/docs/cloud-agent/best-practices)

## Automations

Облачные агенты по расписанию или событию (PR opened, Slack, Linear, webhook…).  
Создание: [cursor.com/automations](https://cursor.com/automations) или `/automate`.

У automations есть свои Memories (отдельно от IDE).

## Упражнения

1. Открой docs/cloud и посмотри требования к environment.
2. Если план позволяет — запусти маленькую cloud-задачу (например, «добавь секцию в README и открой PR»).
3. Допиши в `AGENTS.md` «как проверять изменения в этом репо» — это особенно важно для cloud.

## Готово, когда

Понимаешь разницу local Agent vs Cloud Agent vs Automation.
