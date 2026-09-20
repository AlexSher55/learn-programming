# 2.9 — Enums

Теория **с нуля**. Практика обязательна до контроля.

---

## 1. Зачем enum

Иногда значение может быть только из **закрытого набора**:

- статус заказа: `pending` / `paid` / `shipped`;
- день недели;
- тема UI: `light` / `dark`.

Строки (`'paid'`) легко опечатать. Enum фиксирует набор на уровне типа.

```dart
enum OrderStatus { pending, paid, shipped }

void main() {
  OrderStatus s = OrderStatus.paid;
  print(s); // OrderStatus.paid
}
```

---

## 2. Сравнение и `switch`

```dart
String label(OrderStatus s) {
  switch (s) {
    case OrderStatus.pending:
      return 'Ждём оплату';
    case OrderStatus.paid:
      return 'Оплачен';
    case OrderStatus.shipped:
      return 'Отправлен';
  }
}
```

Если перечислил все значения enum, `default` часто не нужен — компилятор проверяет полноту.

---

## 3. Полезные члены

```dart
print(OrderStatus.paid.name);  // paid — строка
print(OrderStatus.values);     // список всех значений
```

---

## 4. Enhanced enums (кратко)

В Dart enum может иметь поля и методы:

```dart
enum Planet {
  earth(1.0),
  mars(0.38);

  final double gravity;
  const Planet(this.gravity);
}
```

Для Core достаточно знать: enum — не только «голые имена», но может нести данные. Детали — по мере надобности.

---

## 5. Сравнение с JS

В JS часто используют строки или `as const` объекты. Отдельного enum как в Dart исторически не было (есть предложение / TS enums). В Dart enum — полноценный тип.

---

## 6. Типичные ошибки

1. Сравнивать с строкой: `s == 'paid'` вместо `s == OrderStatus.paid`.
2. Хранить статус как `String` «по привычке» из JS.
3. Забыть обновить `switch`, когда добавили новое значение enum.

---

## 7. Чеклист

- объявление `enum`;
- использование значения;
- `switch` по enum;
- `.name`, `.values`.

---

## 8. Практика (обязательно)

Папка: `practice/02-09/`

```bash
dart run practice/02-09/task_01.dart
dart run practice/02-09/task_02.dart
```

**Режим: 🔴.**

---

## Контроль №12

**Режим: 🔴. Проходной: 100%.** Сначала практика.

1. Зачем нужен enum вместо строк?
2. Как объявить enum с тремя статусами и присвоить переменной одно значение?
3. Почему `switch` по enum удобен? Что будет, если добавить новое значение и не обновить `switch`?
4. Что дают `.name` и `.values`?

## После успешной сдачи

Следующая тема: `02-10` — extensions.
