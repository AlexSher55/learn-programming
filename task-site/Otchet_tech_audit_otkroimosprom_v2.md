# Отчёт по вёрстке и фронтенду — Открой#Моспром (v2)

**Сайт:** https://otkroimosprom.ru/

**Примечание по браузерам.** Ошибки ниже — в основном вёрстка/CSS и клиентская логика. В рамках аудита они **повторяются одинаково** в перечисленных браузерах (отдельных «только Safari / только Firefox» критичных отличий по этим багам не выявлено). У каждой проблемы указано: `повторяется в: …`.

---

## Граничные состояния (edge cases) по ширинам 768 / 1024 / 1240 / 1960

Проверка корректности отображения на промежуточных и широких разрешениях.

### Ширина 768px (планшет / узкий десктоп)

1. Контент ЛК и ряда внутренних страниц **сжимается в узкую колонку слева**, справа остаётся **большая пустая зона** — страница не использует ширину окна.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Левое меню ЛК **пропадает** — навигация по разделам кабинета с экрана недоступна (остаются только иконки шапки).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. На главной карточки слайдера предприятий **выезжают за край** экрана (часть заголовков/кнопок «Узнать подробнее» вне вьюпорта).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. В лояльности подписи у плашек баллов **впритык к краям**, текст переносится криво; активная вкладка «Мой баланс» **слегка не совпадает** с рамкой контента.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. Иконки в мобильной шапке стоят **слишком плотно**; отступы контента до края экрана **слишком маленькие**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

### Ширина 1024px

1. Появляется **горизонтальный скролл** (scrollWidth больше ширины окна).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Кнопка «ПРОФИЛЬ» в шапке **обрезается** краем («ПРОФИ…»).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. В профиле кнопки «Редактировать» / «Настройки» **обрезаются** и/или наезжают друг на друга и на карточку.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Фиксированная шапка **уже окна** / ведёт себя нестабильно (зазоры, «прыжки» при скролле).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. На главной — **лишняя пустота** по центру/сбоку, блоки «разъезжаются».  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

### Ширина 1240px

1. В профиле кнопки «Редактировать» и «Настройки» **наслаиваются** друг на друга (нижняя перекрывает верхнюю, текст обрезан).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Блок ЛК (меню + карточка) **прижат влево**, справа остаётся **широкая пустая область**; появляется внутренний скролл контейнера.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Шапка и контент **не выровнены** на всю полезную ширину — ощущение «сайта в половине экрана».  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

### Ширина 1960px (широкий монитор)

1. Фиксированная шапка **не на всю ширину окна** (зазор справа порядка сотен пикселей) — при скролле шапка «прыгает» / не совпадает с контентом.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Контент и шапка **не растягиваются** под широкий экран — большие пустые поля по бокам, компоновка выглядит незавершённой.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## Шапка сайта (на всех страницах)

**Ссылки:** https://otkroimosprom.ru/ , https://otkroimosprom.ru/personal/ и др.

1. Шапка **не помещается** по ширине на части разрешений — элементы сжимаются, обрезаются или уезжают.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Шапка **уезжает влево** при возврате скроллом наверх; справа пустота, меню съезжает относительно контента.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Иногда сверху виден **«призрак» шапки** — второй ряд логотипа/меню.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. На широком экране (в т.ч. **1960**) фиксированная шапка **не на всю ширину**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. Около **1024px** кнопка «Профиль» **обрезается**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

6. Белый текст на ярко‑зелёных кнопках («Войти» / «Профиль») **плохо читается**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

7. Иконка «глаза» **слишком мелкая**; на промежуточных ширинах может **пропадать** из десктоп-шапки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

8. На мобиле иконки шапки стоят **слишком плотно**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

9. Можно открыть **сразу два меню** (бургер сайта и меню ЛК): второе **не закрывает** первое, всё **наслаивается**; оверлей **не перекрывает** шапку и «глаз».  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## Кнопки и ссылки (по сайту)

1. **Не на всех кнопках** есть hover.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. **Не на всех ссылках** есть hover.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Поведение интерактива **не единообразно**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## Поиск (по сайту)

1. Кнопка лупы — `type="button"`: клик **может не запускать** поиск без скрипта.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. На мобиле поиск/фильтр **ломается** (обрезка, наезды).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## Адаптив (общее)

1. На адаптиве текст **слишком крупный**, много скролла.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. На мобиле **слишком большие отступы** между блоками / при этом местами контент **впритык к краю**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Адаптив **неаккуратный** на промежуточных ширинах (дыры, наезды, разная высота карточек).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Около **375px** (Chrome DevTools) — **горизонтальный скролл**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## Контент и кнопки не вмещаются

1. Текст в кнопках **не влезает** («СМОТРЕТЬ ВСЕ» и др.).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. На части разрешений контент **не вмещается** в ширину окна.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Длинные числа/бейджи в «таблетках» **ломают** блоки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/

1. Блок конкурса на телефоне **сжатый**, кнопка «Принять участие!» мелкая.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Фильтры «Возраст / Формат / Направление» на узком экране занимают много места; cookie перекрывает низ.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. У многих картинок **нет alt**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Баннер cookie **перекрывает низ экрана**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. «Смотреть все» — текст **не помещается**; кнопка иногда **в пустоте**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

6. Около **1024px** — **огромная пустая зона** по центру.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

7. Стрелки слайдера «Что посмотреть в этом месяце» **наезжают на заголовок**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/registration/

1. Почти нет проверки обязательных полей на экране.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. «Имя» принимает **любые символы**, включая спецсимволы.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. «Телефон» по сути только **число цифр (10)**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Email почти не валидируется (`@`); кириллица в адресе не отсекается наглядно → риск «Доступ запрещен» при входе.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. Пароль: нет сложности; проверки **после** «Регистрация».  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

6. На странице **нет галочек согласия** (в попапе — есть): два разных UI.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

7. На телефоне/планшете поля **прилипают к краю**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

8. Во всплывающей регистрации валидация тоже слабая; телефон можно оставить недописанным.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## Формы записи на экскурсии / лекции и конкурс

1. Обязательные поля **не отмечены**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Валидация почти отсутствует (в т.ч. паспорт без формата/длины).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Email — по сути только `@`.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. «Кривая» форма **успешно отправляется** (уведомление / запись в ЛК).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. **Возрастной ценз не учитывается** на форме.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

6. Форма конкурса: слабая валидация; файл **не отображается** после выбора; email проверяется после отправки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/events/ (Навигатор)

1. Сначала видны **статьи**, а не экскурсии.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. «+ Создать экскурсию» **путает** обычного пользователя.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Длинные фильтры на телефоне — много скролла.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Длинные названия карточек **ломают** вёрстку.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. Карточки **разной высоты** в одном ряду.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/contacts/

1. Неактивная «Отправить» без понятной подсказки про согласия.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Белый текст на зелёной кнопке **слабо читается**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Форма на части ширин **прижата** или с лишней пустотой.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/about/

Отдельных проблем не обнаружено (кроме общих по адаптиву).

---

## https://otkroimosprom.ru/projects/

1. На заголовок «Проекты» **наезжает** контент снизу.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Карточки проектов **разной высоты**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. В календаре карточки **разной высоты**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Нет **сброса фильтров** в календаре.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. Показываются **прошедшие мероприятия** без явной пометки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/news/

1. На планшете/мобиле **много пустого пространства** между текстом и фото.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Фото **ниже** текстового блока — дыра под картинкой.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/space/

Отдельных проблем не обнаружено (кроме общих по адаптиву).

---

## https://otkroimosprom.ru/policy/

Отдельных проблем не обнаружено (кроме крупного текста на мобиле).

---

## https://otkroimosprom.ru/rules/

1. Маркированные списки **криво сверстаны** (точки как отдельные символы).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/cookies

1. В таблицах текст **слипается**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. На мобиле таблицы **не адаптируются**, контент обрезается.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/enterprise/

1. Раздел открывает главную — **список предприятий недоступен** как отдельная страница.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/enterprise/firma-cheremushki/

Отдельных проблем на карточке не обнаружено.

---

## Левое меню ЛК (/personal/…)

1. Меню **ломается** на части разрешений (наезды, съезд пунктов).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. На мобиле / ~768 меню **пропадает**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. На телефоне **непонятно**, как переключать разделы ЛК.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/personal/ (профиль)

1. Баг шапки при скролле наверх.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. ~1024 — «Профиль» в шапке обрезается.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Длинные числа баллов ломают плашки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Пустой телефон без заглушки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. «Редактировать» / «Настройки» обрезаются и **наезжают** (в т.ч. на **1240**).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

6. Карточка профиля ломается на ~1023 и уже; на **1240/1960** контент **не заполняет** ширину.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

7. Смена **даты рождения** не срабатывает (datepicker/JS).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/personal/history/

1. «Нет записей» — нет понятного следующего шага.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/personal/loyalty/

1. Подписи у плашек баллов **обрезаются**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Длинные числа баллов съедают место.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. Две цены на карточке мерча **наезжают** на узком экране.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Блоки внутри карточек мерча **съезжают**, отступы разные.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. «Обменять» — текст **впритык** к краям кнопки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

6. На части разрешений контент обрезается / уезжает; на **768** — узкая колонка и пустота справа.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/personal/quiz/

1. Стрелка в «Пройти квиз» **не по центру**.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

2. Длинные бейджи баллов могут не вмещаться.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

3. На части разрешений контент «плывёт», шапка/меню наезжают.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

4. Счётчик «Текущие **(3)**» при **2** карточках.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

5. После прохождения список **не обновляется** без ухода со вкладки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

6. В модалке квиза текст **наезжает** на крестик.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

7. Оверлей квиза **не перекрывает** шапку и иконки.  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## https://otkroimosprom.ru/personal/contest/ (Конкурс в ЛК) — новое

1. Страница `/personal/contest/` открывается с заголовком **«Карта сайта»** вместо формы/контента конкурса — раздел выглядит **сломанным** (контент конкурса не отображается).  
   **повторяется в:** Google Chrome, Safari, Яндекс.Браузер, Mozilla Firefox, Opera, Microsoft Edge

---

## Что тестировалось (публичная часть и ЛК)

1. Формы регистрации и авторизации, граничные значения полей.  
2. Личный кабинет: профиль, записи, лояльность, квизы, конкурс.  
3. Запись на экскурсии/лекции.  
4. Обработка данных в формах на стороне интерфейса.  
5. Cookie / политики с точки зрения UI.  
6. Фильтры, поиск, навигация.  
7. Лояльность.  
8. Предприятия и раздел `/enterprise/`.  
9. User flow: главная → запись/регистрация → ЛК → лояльность/квизы/история.  
10. Edge cases по ширинам **768, 1024, 1240, 1960**.

---

## Кросс-браузерное и адаптивное тестирование

Обеспечена проверка корректности работы Портала на различных устройствах и в различных средах, включая:

- десктопные устройства (Windows, macOS — macOS через эмулятор);
- мобильные устройства (iOS, Android) на реальных устройствах;
- планшеты.

Тестирование проведено в актуальных версиях браузеров, включая:

- Google Chrome;
- Safari;
- Яндекс.Браузер;
- Mozilla Firefox;
- Opera;
- Microsoft Edge.

В рамках тестирования:

- проверена корректность вёрстки на различных разрешениях экранов (включая нестандартные и промежуточные разрешения: **768, 1024, 1240, 1960** и др.);
- выявлены ошибки адаптивной вёрстки (смещения, наложения элементов, некорректные отступы и масштабирование);
- проверена корректность отображения интерактивных элементов (кнопки, формы, выпадающие списки);
- оценено удобство пользовательского взаимодействия на мобильных устройствах (mobile UX);
- проверена корректность загрузки и отображения мультимедийного контента.

**Итог:** проблемы на разных системах и в разных браузерах **по сути те же**. Критичных отличий вида «только один браузер» по описанным ошибкам вёрстки не выявлено.
