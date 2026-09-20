# 2.12 — Exceptions

Теория **с нуля**. Практика обязательна до контроля.

---

## 1. Зачем exceptions

Иногда операция **не может** нормально завершиться: нет файла, деление на ноль, неверный аргумент. Нужен способ сказать: «ошибка» — и либо обработать, либо пробросить выше.

```dart
int parseAge(String raw) {
  return int.parse(raw); // если raw = 'abc' → выбросит FormatException
}
```

---

## 2. `try` / `catch` / `finally`

```dart
void main() {
  try {
    var age = int.parse('abc');
    print(age);
  } on FormatException catch (e) {
    print('bad format: $e');
  } catch (e) {
    print('other: $e');
  } finally {
    print('always');
  }
}
```

Порядок:
1. Выполняется `try`.
2. Если бросили исключение подходящего типа — `on Type catch`.
3. Общий `catch` — любые остальные.
4. `finally` — **всегда** (и при успехе, и при ошибке): закрыть ресурс, залогировать конец, и т.п.

---

## 3. `throw` и `rethrow`

```dart
void ensurePositive(int n) {
  if (n <= 0) {
    throw ArgumentError('n must be > 0');
  }
}
```

`rethrow` — поймали, что-то сделали (лог), и **пробросили дальше** то же исключение:

```dart
try {
  ensurePositive(-1);
} catch (e) {
  print('log: $e');
  rethrow;
}
```

---

## 4. Exception vs Error (кратко)

В Dart:
- `Exception` — ожидаемые сбои («не распарсилось»), которые часто ловят;
- `Error` — программные ошибки (баг: `ArgumentError` иногда сюда ближе по духу использования, но иерархия своя).

Для Core: лови то, что можешь осмысленно обработать; не глуши всё пустым `catch` без логов.

---

## 5. Сравнение с JS

| JS | Dart |
|---|---|
| `try/catch/finally` | то же |
| `throw` | `throw` |
| `catch (e)` | `catch (e)` / `on Type catch (e)` |
| нет `rethrow` как слова | есть `rethrow` |

---

## 6. Типичные ошибки

1. Пустой `catch` — ошибка проглочена, отладка ад.
2. Ловить слишком широко и не различать типы.
3. Использовать exceptions для обычного control flow («вместо if»).

---

## 7. Чеклист

- `try` / `on` / `catch` / `finally`;
- `throw`;
- `rethrow`;
- не глотать ошибки молча.

---

## 8. Практика (обязательно)

Папка: `practice/02-12/`

```bash
dart run practice/02-12/task_01.dart
dart run practice/02-12/task_02.dart
```

**Режим: 🔴.**

---

## Контроль №15

**Режим: 🔴. Проходной: 100%.** Сначала практика.

1. Зачем нужны exceptions? Чем это отличается от обычного `return`?
2. Разбери порядок: `try` → `on FormatException` → `catch` → `finally`. Когда выполняется `finally`?
3. Что делает `throw`? Приведи пример с неверным аргументом.
4. Зачем `rethrow`?
5. Почему плох пустой `catch (e) {}`?

## После успешной сдачи

Раздел 2 (Dart Core) закрыт. Дальше — Раздел 3 (Algorithms I + Big O); тексты пока skeleton в `lessons/README.md`, агент допишет при переходе.
