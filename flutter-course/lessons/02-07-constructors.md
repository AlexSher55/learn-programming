# 2.7 — Constructors

Теория **с нуля**. Практика обязательна до контроля.

Нужен `02-06` (классы).

---

## 1. Зачем конструктор

Конструктор — специальный код, который **создаёт** объект и обычно заполняет поля.

Имя совпадает с именем класса:

```dart
class User {
  final String name;
  final int age;

  User(this.name, this.age); // generative constructor
}
```

`User('Alex', 25)` вызывает этот конструктор.

---

## 2. Именованные конструкторы

У класса может быть несколько способов создания:

```dart
class User {
  final String name;
  final int age;

  User(this.name, this.age);

  User.guest()
      : name = 'Guest',
        age = 0;

  User.fromMap(Map<String, Object> map)
      : name = map['name'] as String,
        age = map['age'] as int;
}
```

Вызов:

```dart
var a = User('Alex', 25);
var b = User.guest();
var c = User.fromMap({'name': 'Sam', 'age': 30});
```

После `:` — **initializer list**: поля заполняются до тела конструктора.

---

## 3. `const` конструкторы

Если все поля — `final` и значения известны на compile-time, можно:

```dart
class Point {
  final int x;
  final int y;

  const Point(this.x, this.y);
}

const origin = Point(0, 0);
var p = const Point(1, 2);
```

`const` объект канонически переиспользуется: два `const Point(0, 0)` могут быть одним и тем же каноническим экземпляром. Для Core запомни: **compile-time + неизменяемый**.

---

## 4. `factory` конструкторы

`factory` — конструктор, который **не обязан** всегда создавать новый объект. Может вернуть уже существующий или объект другого подтипа.

```dart
class Logger {
  static final Logger _instance = Logger._();

  factory Logger() => _instance;

  Logger._(); // приватный generative
}
```

```dart
var a = Logger();
var b = Logger();
print(identical(a, b)); // true — один и тот же объект
```

На уровне Core достаточно идеи: `factory` = «создай или верни по своим правилам», не обычное `this.field = ...` напрямую в сигнатуре.

---

## 5. Сравнение с JS

| JS | Dart |
|---|---|
| `constructor()` | `Class(...)` |
| static factory-методы | часто `factory` / named constructors |
| нет `const` объектов как в Dart | `const` constructor — важная идея Flutter |

---

## 6. Типичные ошибки

1. Путать named constructor `User.guest()` с методом.
2. Забыть `const` у конструктора, но писать `const Point(0,0)`.
3. Думать, что `factory` всегда создаёт новый объект.

---

## 7. Чеклист

- обычный конструктор;
- named constructor + initializer list;
- `const` constructor;
- идея `factory`.

---

## 8. Практика (обязательно)

Папка: `practice/02-07/`

```bash
dart run practice/02-07/task_01.dart
dart run practice/02-07/task_02.dart
```

**Режим: 🔴.**

---

## Контроль №10

**Режим: 🔴. Проходной: 100%.** Сначала практика.

1. Зачем нужен конструктор? Когда он вызывается?
2. Что такое именованный конструктор? Приведи пример вызова.
3. Что такое initializer list (`: name = ...`)?
4. Какие условия нужны, чтобы сделать `const` конструктор? Зачем он?
5. Чем идея `factory` отличается от обычного generative-конструктора?

## После успешной сдачи

Следующая тема: `02-08` — наследование и композиция.
