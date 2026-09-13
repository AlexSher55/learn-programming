# Прогресс — Dart / Flutter

Этот файл — главный сейв учебного трека. На любом устройстве: `git pull` → открыть проект → попросить агента прочитать `flutter-course/PROGRESS.md` и продолжить.

## Цель

Стать крепким Flutter-разработчиком уровня middle: фундамент CS, алгоритмы и структуры данных, глубокий Dart, Flutter internals, state management, architecture, data layer, testing, performance, native/platform integration и production release.

## Исходный уровень

- Профессия: frontend developer.
- Известно: HTML, CSS, JavaScript (частично), немного Vue/Nuxt, Git.
- Самооценка алгоритмов на старте: 3/10.
- Режим: жёсткий, без поблажек.
- График: обычно 2–4 часа, нерегулярно, параллельно с работой 5/2.

## Сейчас

- **Раздел:** 2 — Dart Core
- **Тема:** 2.3 — функции: параметры, named/optional/required, `=>`
- **Статус:** теория расширена «с нуля»; контроль №6 ещё не отвечен
- **Режим:** 🔴 AI forbidden
- **Следующий шаг:** прочитать полный `lessons/02-03-functions.md`, затем ответить на контроль №6
- **Обновлено:** 2026-09-13
- **Заметка по стилю:** теория далее — обширная, для новичка Dart/Flutter; контроль только по материалу урока

## Уже закрыто на 100%

### Диагностика

Стартовая диагностика показала основные пробелы:
- Big O и анализ сложности;
- структуры данных и базовые алгоритмы;
- stack/heap/call stack;
- event loop/async;
- реализация алгоритмов с нуля.

Сильные стороны на старте:
- практический frontend-опыт;
- базовое понимание ссылок;
- инженерная интуиция по API/pagination/server-side filtering.

### Раздел 1 — Как работает программа

Конспекты:
- `lessons/01-01-cpu-ram.md`
- `lessons/01-02-stack-heap-gc.md`
- `lessons/01-03-value-reference-mutation.md`

Закрыто:
- CPU: Fetch → Decode → Execute.
- RAM как рабочая память программы.
- Индекс массива ≠ адрес памяти.
- Упрощённая формула адреса элемента: `baseAddress + index * elementSize`.
- Один объект может иметь несколько ссылок.

### Stack / Heap / Call Stack / GC

Закрыто:
- LIFO;
- stack frame;
- call stack;
- причина stack overflow при бесконечной рекурсии;
- heap как модель хранения динамических объектов;
- достижимость объекта;
- GC может очистить недостижимый объект;
- `return;` / отсутствие return в JS возвращает `undefined`, объект сам по себе не возвращается.

### Value / Reference / Mutation / Shallow Copy

Закрыто:
- копирование простого значения даёт независимые значения;
- присваивание объекта копирует ссылку, а не объект;
- две переменные могут ссылаться на один объект;
- mutation = изменение уже существующего объекта через ссылку;
- spread верхнего уровня создаёт новый внешний объект;
- shallow copy сохраняет общие ссылки на вложенные объекты.

Ключевая формулировка, которую пользователь усвоил:
> `a` и `b` могут хранить ссылки на один объект; сами ссылки не меняются, а через одну из них можно мутировать общий объект.

### 2.1 — `var` / `final` / `const`

Конспект: `lessons/02-01-var-final-const.md` (расширен после сдачи).

Контроль №4 сдан со второй попытки.

Закрыто:
- `var` фиксирует тип выводом и разрешает переприсваивание внутри этого типа;
- `final` запрещает переприсваивание имени; mutable-объект по ссылке можно мутировать;
- `const` — compile-time, объект заморожен;
- `DateTime.now()` нельзя сделать `const`;
- слот / ссылка / объект не смешиваются с переприсваиванием.

Уточнение, которое нельзя потерять: в учебной модели `int` лежит в слоте как значение; в Dart `int` всё же объект, но неизменяемый.

### 2.2 — Типовая система

Конспект: `lessons/02-02-types.md` (расширен после сдачи).

Контроль №5 сдан с пересдач.

Закрыто:
- `int` / `double` / `num`;
- `/` → `double`, `~/` → `int`;
- `String` vs `String?` (null safety);
- `Object` хранит что угодно ненулевое, но не даёт члены конкретного типа;
- `dynamic` — компилятор почти не проверяет вызовы; присваивание другого значения у `dynamic` ок;
- `var` ≠ `dynamic`; к JS-`let` ближе `dynamic`.

## Карта курса

| # | Раздел | Статус |
|---|---|---|
| 0 | Диагностика | done |
| 1 | CS foundation: CPU/RAM/stack/heap/references | done |
| 2 | Dart Core | in_progress |
| 3 | Algorithms I + Big O | todo |
| 4 | Data Structures | todo |
| 5 | Dart Advanced: async, Future, Stream, event loop, isolates | todo |
| 6 | Flutter Core: Widget/Element/RenderObject, layout, lifecycle, keys | todo |
| 7 | UI Engineering | todo |
| 8 | State Management | todo |
| 9 | Data Layer: API, persistence, cache, offline | todo |
| 10 | Architecture / DI / feature design | todo |
| 11 | Testing / debugging / quality | todo |
| 12 | Performance / DevTools | todo |
| 13 | Mobile platform / permissions / deep links / push | todo |
| 14 | Production / flavors / CI/CD / release | todo |
| 15 | Middle capstone project | todo |

## Правила прохождения

- Фундаментальные темы: проходной балл 100%.
- Остальные проверки: ориентир 90%+, но пробелы всё равно закрываются пересдачей.
- На 🔴 задачах нельзя использовать AI для получения ответа.
- Ошибка → объяснение механизма → короткая пересдача → только затем следующий блок.
- Старые темы должны периодически появляться в новых задачах.

## Как продолжить на другом ПК

1. `git pull`
2. Открыть репозиторий в Cursor.
3. Написать агенту: `Прочитай flutter-course/AGENTS.md и flutter-course/PROGRESS.md. Продолжим с текущего места.`
4. Выполнить текущую задачу самостоятельно, если режим 🔴.
5. После проверки попросить агента обновить `flutter-course/PROGRESS.md`.
6. `git add . && git commit -m "course: update flutter progress" && git push`

## Как продолжить в ChatGPT

Лучший вариант — загрузить сюда:
- `flutter-course/PROGRESS.md`;
- файл текущего урока;
- при необходимости файл с решением/кодом.

Можно также прислать ZIP репозитория, но `.git/` для продолжения урока не нужен.
