# 2.1 — Dart: `var`, `final`, `const`

## Короткая теория

### `var`

Dart выводит тип по начальному значению:

```dart
var age = 25; // inferred as int
age = 30;     // ok
// age = 'Alex'; // error: String is not int
```

### `final`

Значение переменной присваивается один раз, но объект может оставаться mutable:

```dart
final numbers = [1, 2, 3];
numbers.add(4);       // ok: мутируем тот же List
// numbers = [10, 20]; // error: переприсваиваем final
```

### `const`

Compile-time constant. Const-коллекция неизменяема:

```dart
const numbers = [1, 2, 3];
// numbers.add(4); // попытка изменения const List недопустима
```

`final` может получить runtime-значение:

```dart
final now = DateTime.now();
```

Но `const` требует compile-time constant:

```dart
// const now = DateTime.now(); // invalid
```

## Контроль №4

**Режим: 🔴 AI forbidden. Проходной: 100%.**

Ответь своими словами, не копируя определения.

1. В чём разница между:

```dart
var age = 25;
```

и:

```dart
final age = 25;
```

2. Почему это работает:

```dart
final numbers = [1, 2, 3];
numbers.add(4);
```

но это не работает:

```dart
numbers = [10, 20];
```

Объясни через ссылку и объект.

3. Что произойдёт здесь и почему?

```dart
const numbers = [1, 2, 3];
numbers.add(4);
```

4. Почему допустимо:

```dart
final now = DateTime.now();
```

а это нет:

```dart
const now = DateTime.now();
```

5. Что произойдёт:

```dart
var value = 10;
value = 20;
value = 'Alex';
```

Какая строка допустима, какая нет и почему?

6. Объясни junior-разработчику разницу между `final` и `const` своими словами.

## После успешной сдачи

Следующая тема: типовая система Dart — `int`, `double`, `num`, `String`, `bool`, `Object`, `Object?`, `dynamic` и вывод типов.
