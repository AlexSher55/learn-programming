# Уроки Flutter/Dart курса

Читай по порядку. Источник прогресса: [`../PROGRESS.md`](../PROGRESS.md).

Статусы: `closed` — закрыто · `in_progress` — текущий · `full` — текст готов, ещё не начат · `skeleton` — только название, текста пока нет · `optional_practice` — теория закрыта, практика для закрепления.

## Как проходить урок

1. Прочитать теорию в файле урока.
2. Сделать практику в `../practice/XX-YY/` (`dart run task_01.dart` и т.д.).
3. Написать агенту: «проверь практику» (или путь к файлам).
4. Сдать контроль в чате (🔴 — своими силами).
5. Агент обновит `PROGRESS.md`.

---

## Раздел 1 — CS foundation

| Файл | Тема | Статус |
|---|---|---|
| [01-01-cpu-ram.md](01-01-cpu-ram.md) | CPU, RAM, индекс vs адрес | closed |
| [01-02-stack-heap-gc.md](01-02-stack-heap-gc.md) | Stack, heap, call stack, GC | closed |
| [01-03-value-reference-mutation.md](01-03-value-reference-mutation.md) | Value / reference / mutation / shallow copy | closed |

## Раздел 2 — Dart Core

| Файл | Тема | Статус |
|---|---|---|
| [02-01-var-final-const.md](02-01-var-final-const.md) | `var` / `final` / `const` | closed + optional_practice |
| [02-02-types.md](02-02-types.md) | Типы, null safety, `Object` / `dynamic` | closed + optional_practice |
| [02-03-functions.md](02-03-functions.md) | Функции, параметры, `=>` | in_progress |
| [02-04-control-flow.md](02-04-control-flow.md) | `if` / `switch` / циклы | full |
| [02-05-collections.md](02-05-collections.md) | `List` / `Set` / `Map` | full |
| [02-06-classes.md](02-06-classes.md) | Классы и поля | full |
| [02-07-constructors.md](02-07-constructors.md) | Конструкторы | full |
| [02-08-inheritance-composition.md](02-08-inheritance-composition.md) | Наследование и композиция | full |
| [02-09-enums.md](02-09-enums.md) | Enums | full |
| [02-10-extensions.md](02-10-extensions.md) | Extensions | full |
| [02-11-generics.md](02-11-generics.md) | Generics (основы) | full |
| [02-12-exceptions.md](02-12-exceptions.md) | Exceptions | full |

## Раздел 3 — Algorithms I + Big O

| Файл | Тема | Статус |
|---|---|---|
| 03-01-big-o.md | Big O, рост функций | skeleton |
| 03-02-linear-binary-search.md | Линейный и бинарный поиск | skeleton |
| 03-03-sorting-basics.md | Основы сортировок | skeleton |
| 03-04-recursion.md | Рекурсия | skeleton |
| 03-05-two-pointers-sliding-window.md | Two pointers, sliding window | skeleton |
| 03-06-frequency-maps.md | Frequency maps | skeleton |

## Раздел 4 — Data Structures

| Файл | Тема | Статус |
|---|---|---|
| 04-01-list-array.md | List / массив | skeleton |
| 04-02-string.md | String как структура | skeleton |
| 04-03-stack-queue.md | Stack, Queue | skeleton |
| 04-04-set-map.md | Set, Map / HashMap | skeleton |
| 04-05-linked-list.md | Linked List | skeleton |
| 04-06-tree-heap.md | Tree, Heap | skeleton |
| 04-07-graph.md | Graph | skeleton |

## Раздел 5 — Dart Advanced

| Файл | Тема | Статус |
|---|---|---|
| 05-01-future-async-await.md | Future, async/await | skeleton |
| 05-02-event-loop.md | Microtasks / event queue | skeleton |
| 05-03-streams.md | Stream | skeleton |
| 05-04-isolates.md | Isolates | skeleton |
| 05-05-records-patterns.md | Records, patterns | skeleton |
| 05-06-mixins-sealed.md | Mixins, sealed types | skeleton |
| 05-07-advanced-generics.md | Advanced generics | skeleton |

## Раздел 6 — Flutter Core

| Файл | Тема | Статус |
|---|---|---|
| 06-01-widget-element-renderobject.md | Widget / Element / RenderObject | skeleton |
| 06-02-buildcontext-constraints.md | BuildContext, constraints / layout | skeleton |
| 06-03-lifecycle.md | Lifecycle | skeleton |
| 06-04-keys.md | Keys | skeleton |
| 06-05-navigation.md | Navigation | skeleton |

## Раздел 7 — UI Engineering

| Файл | Тема | Статус |
|---|---|---|
| 07-01-responsive-adaptive.md | Responsive / adaptive UI | skeleton |
| 07-02-forms-validation.md | Forms, validation | skeleton |
| 07-03-animations.md | Animations | skeleton |
| 07-04-a11y-l10n.md | Accessibility, localization | skeleton |
| 07-05-design-systems.md | Design systems | skeleton |

## Раздел 8 — State Management

| Файл | Тема | Статус |
|---|---|---|
| 08-01-local-state.md | Local state first | skeleton |
| 08-02-state-principles.md | Принципы и сравнение подходов | skeleton |
| 08-03-immutable-updates.md | Immutable state, predictable updates | skeleton |

## Раздел 9 — Data Layer

| Файл | Тема | Статус |
|---|---|---|
| 09-01-rest-serialization.md | REST, serialization | skeleton |
| 09-02-repositories.md | Repositories / services | skeleton |
| 09-03-auth.md | Authentication | skeleton |
| 09-04-persistence-cache.md | Persistence, caching | skeleton |
| 09-05-pagination-offline.md | Pagination, offline-first | skeleton |

## Раздел 10 — Architecture

| Файл | Тема | Статус |
|---|---|---|
| 10-01-separation-of-concerns.md | Separation of concerns | skeleton |
| 10-02-feature-first.md | Feature-first structure | skeleton |
| 10-03-di.md | DI | skeleton |
| 10-04-domain-errors.md | Domain layer, error modeling | skeleton |

## Раздел 11 — Quality

| Файл | Тема | Статус |
|---|---|---|
| 11-01-unit-widget-tests.md | Unit / widget tests | skeleton |
| 11-02-integration-mocks.md | Integration, mocks / fakes | skeleton |
| 11-03-debugging-logging.md | Debugging, logging | skeleton |
| 11-04-review-refactor.md | Code review, refactoring | skeleton |

## Раздел 12 — Performance

| Файл | Тема | Статус |
|---|---|---|
| 12-01-rebuilds-rendering.md | Rebuilds, rendering | skeleton |
| 12-02-lists-images.md | Lists, image / memory | skeleton |
| 12-03-devtools-profiling.md | DevTools, profiling | skeleton |
| 12-04-isolates-cpu.md | CPU-heavy work, isolates | skeleton |

## Раздел 13 — Mobile platform

| Файл | Тема | Статус |
|---|---|---|
| 13-01-lifecycle-permissions.md | Android/iOS lifecycle, permissions | skeleton |
| 13-02-deep-links-push.md | Deep links, notifications | skeleton |
| 13-03-platform-channels.md | Platform channels | skeleton |

## Раздел 14 — Production

| Файл | Тема | Статус |
|---|---|---|
| 14-01-flavors-secrets.md | Flavors, secrets | skeleton |
| 14-02-analytics-crash.md | Analytics, crash reporting | skeleton |
| 14-03-cicd-release.md | CI/CD, signing, stores | skeleton |

## Раздел 15 — Capstone

| Файл | Тема | Статус |
|---|---|---|
| 15-01-capstone.md | Production-like app end-to-end | skeleton |
