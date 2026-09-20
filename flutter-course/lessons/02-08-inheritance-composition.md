# 2.8 — Inheritance и composition

Теория **с нуля**. Практика обязательна до контроля.

Нужен `02-06`–`02-07`.

---

## 1. Две идеи переиспользования

Хочешь переиспользовать код. Два основных пути:

1. **Inheritance (наследование)** — «B — это разновидность A» (`Dog` is-a `Animal`).
2. **Composition (композиция)** — «B **содержит** A» (`Car` has-a `Engine`).

В Flutter/Dart чаще предпочитают композицию, но наследование тоже нужно понимать.

---

## 2. Наследование: `extends`

```dart
class Animal {
  void speak() => print('...');
}

class Dog extends Animal {
  @override
  void speak() => print('woof');
}
```

`Dog` получает члены `Animal` и может **переопределить** (`@override`) метод.

```dart
Animal a = Dog();
a.speak(); // woof — вызывается реализация Dog
```

Переменная типа `Animal` может ссылаться на объект `Dog` (подтип). Вызов метода идёт по **реальному** объекту.

### `super`

```dart
class Animal {
  final String name;
  Animal(this.name);
}

class Dog extends Animal {
  Dog(String name) : super(name);
}
```

`super(...)` вызывает конструктор родителя.

---

## 3. Абстрактные классы (кратко)

```dart
abstract class Shape {
  double area();
}

class Circle extends Shape {
  final double r;
  Circle(this.r);

  @override
  double area() => 3.14 * r * r;
}
```

`abstract class` нельзя создать через `Shape()` напрямую — только через конкретный подкласс. Метод без тела — обязанность потомка.

---

## 4. Композиция

```dart
class Engine {
  void start() => print('vroom');
}

class Car {
  final Engine engine;
  Car(this.engine);

  void start() => engine.start();
}
```

`Car` не «является» `Engine`, а **держит** его. Гибче: можно подставить другой engine.

---

## 5. Когда что выбирать

| Вопрос | Скорее |
|---|---|
| B **является** разновидностью A? | inheritance |
| B **использует** A как деталь? | composition |
| Нужно подставить разное поведение снаружи? | composition |

Ошибка новичка: глубокие цепочки `extends` «на всякий случай». Лучше короткие иерархии + композиция.

---

## 6. Сравнение с JS

Прототипное наследование в JS другое под капотом. Синтаксис `class Child extends Parent` похож, но модель типов в Dart строже (статические типы).

---

## 7. Типичные ошибки

1. Путать is-a и has-a.
2. Забыть `@override` (не всегда ошибка компиляции, но плохая привычка).
3. Забыть вызвать `super` в конструкторе потомка, когда родитель требует аргументы.

---

## 8. Чеклист

- `extends`, `@override`, `super`;
- подтип: `Animal a = Dog()`;
- abstract class (идея);
- composition has-a;
- когда inheritance, когда composition.

---

## 9. Практика (обязательно)

Папка: `practice/02-08/`

```bash
dart run practice/02-08/task_01.dart
dart run practice/02-08/task_02.dart
```

**Режим: 🔴.**

---

## Контроль №11

**Режим: 🔴. Проходной: 100%.** Сначала практика.

1. Что значит `class Dog extends Animal`?
2. Зачем `@override`? Что происходит при `Animal a = Dog(); a.speak();`, если `speak` переопределён в `Dog`?
3. Зачем `super` в конструкторе потомка?
4. Чем композиция отличается от наследования? Приведи короткий пример has-a.
5. Когда разумнее композиция, а не `extends`?

## После успешной сдачи

Следующая тема: `02-09` — enums.
