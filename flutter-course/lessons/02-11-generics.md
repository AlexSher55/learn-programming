# 2.11 — Generics (основы)

Теория **с нуля**. Практика обязательна до контроля.

Связь: коллекции (`02-05`), классы (`02-06`).

---

## 1. Зачем generics

Хочешь «коробку», которая работает с **разными** типами, но без потери проверки типов.

Плохо (теряем тип):

```dart
class Box {
  dynamic value;
  Box(this.value);
}
```

Хорошо:

```dart
class Box<T> {
  T value;
  Box(this.value);
}

var a = Box<int>(10);
var b = Box<String>('hi');
// a.value — int
// b.value — String
```

`T` — **параметр типа**. Подставляешь конкретный тип при использовании.

---

## 2. Уже видел generics

```dart
List<int> nums = [1, 2];
Map<String, int> ages = {'Alex': 25};
```

`List` — по сути «список элементов типа E». Без `<int>` вывод часто сработает из литерала, но явно писать полезно.

---

## 3. Generic-функции

```dart
T first<T>(List<T> items) {
  return items[0];
}

print(first<int>([10, 20]));     // 10
print(first(['a', 'b']));        // String выведется
```

---

## 4. Ограничения (`extends`)

Иногда «любой T» слишком широко — нужно, чтобы T умел что-то:

```dart
num sum<T extends num>(T a, T b) => a + b;

sum(1, 2);     // ок
sum(1.5, 2.0); // ок
// sum('a', 'b'); // ошибка
```

---

## 5. Зачем это в Flutter

Виджеты и коллекции постоянно параметризованы: `ListView`, `FutureBuilder<T>`, и т.д. Без generics пришлось бы везде `dynamic` и терять проверки.

---

## 6. Сравнение с JS

В JS типы в runtime почти нет; generics — идея из TypeScript. В Dart generics есть и в языке, и в runtime-модели (с оговорками; для Core: компилятор проверяет `T`).

---

## 7. Типичные ошибки

1. Писать `List` без типа и класть туда всё подряд → получается `List<dynamic>` и сюрпризы.
2. Путать параметр типа `T` с обычным параметром функции.
3. Думать, что `Box<int>` и `Box<String>` — один и тот же тип.

---

## 8. Чеклист

- `class Foo<T>`;
- `List<T>`, `Map<K,V>`;
- generic-функция;
- `T extends NumLike`.

---

## 9. Практика (обязательно)

Папка: `practice/02-11/`

```bash
dart run practice/02-11/task_01.dart
dart run practice/02-11/task_02.dart
```

**Режим: 🔴.**

---

## Контроль №14

**Режим: 🔴. Проходной: 100%.** Сначала практика.

1. Зачем нужны generics? Чем `Box<T>` лучше `Box` с `dynamic value`?
2. Что означает `List<int>`? Чем это отличается от `List<String>`?
3. Разбери `T first<T>(List<T> items)`.
4. Зачем `T extends num` в generic-функции?
5. Почему `List` без параметра типа часто приводит к проблемам?

## После успешной сдачи

Следующая тема: `02-12` — exceptions.
