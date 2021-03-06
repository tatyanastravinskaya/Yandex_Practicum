# Выпускной проект

## Данные

Выпускной проект состоит из трех частей:
### 1. Анализ поведения пользователей в мобильном приложении.
**Данные**

В нашем распоряжении данные о событиях, совершенных в мобильном приложении "Ненужные вещи". В нем пользователи продают свои ненужные вещи, размещая их на доске объявлений. В датасете содержатся данные пользователей, впервые совершивших действия в приложении после 7 октября 2019 года.

Колонки в ***mobile_sources.csv***:
* `user_id` — идентификатор пользователя;
* `source` — источник, с которого пользователь установил приложение.

Колонки в ***mobile_dataset.csv***:
* `event_time` — время совершения;
* `user_id` — идентификатор пользователя;
* `event_name` — действие пользователя. Виды действий:
* `advert_open` — открыл карточки объявления;
* `photos_show` — просмотрел фотографий в объявлении;
* `tips_show` — увидел рекомендованные объявления;
* `tips_click` — кликнул по рекомендованному объявлению;
* `contacts_show` и `show_contacts` — посмотрел номер телефона;
* `contacts_call` — позвонил по номеру из объявления;
* `map` — открыл карту объявлений;
* `search_1` — `search_7` — разные действия, связанные с поиском по сайту;
* `favorites_add` — добавил объявление в избранное.

**Цели исследования:**
* Проанализировать связь целевого события - просмотра контактов - и других действий пользователей.
* Оценить, какие действия чаще совершают те пользователи, которые просматривают контакты.

**Задачи исследования:**
* Провести исследовательский анализ данных.
* Проанализировать влияние событий на совершение целевого события.
* Проверить статистические гипотезы.
* Дать общие выводы и рекомендации.

**Используемые библиотеки:**
* *pandas*;
* *datetime*;
* *matplotlib*;
* *numpy*;
* *plotly*;
* *seaborn*;
* *math*;
* *scipy*.

### 2. Проект по А/B-тестированию
**Задача** - провести оценку результатов А/В-теста:
1.  Оценить корректность проведения теста:
* пересечение тестовой аудитории с конкурирующим тестом;
* совпадение теста и маркетинговых событий, другие проблемы временных границ теста.
2. Проанализировать результаты теста.

**Техническое задание**
1. Название теста: `recommender_system_test`;
2. группы: А — контрольная, B — новая платёжная воронка;
3. дата запуска: 2020-12-07;
4. дата остановки набора новых пользователей: 2020-12-21;
5. дата остановки: 2021-01-04;
6. аудитория: 15% новых пользователей из региона EU;
7. назначение теста: тестирование изменений, связанных с внедрением улучшенной рекомендательной системы;
8. ожидаемое количество участников теста: 6000.
9. ожидаемый эффект: за 14 дней с момента регистрации пользователи покажут улучшение каждой метрики не менее, чем на 10%:
* конверсии в просмотр карточек товаров — событие product_page;
* просмотры корзины — product_cart;
* покупки — purchase.

**Используемые библиотеки:**
* *pandas*;
* *datetime*;
* *matplotlib*;
* *numpy*;
* *plotly*;
* *math*;
* *scipy*.

### 3. Проект по SQL
Коронавирус застал мир врасплох, изменив привычный порядок вещей. В свободное время жители городов больше не выходят на улицу, не посещают кафе и торговые центры. Зато стало больше времени для книг. Это заметили стартаперы — и бросились создавать приложения для тех, кто любит читать. Наша компания решила быть на волне и купила крупный сервис для чтения книг по подписке. Наша первая задача — проанализировать базу данных. В ней — информация о книгах, издательствах, авторах, а также пользовательские обзоры книг. Эти данные помогут сформулировать ценностное предложение для нового продукта.

**Задача** - ответить на вопросы:
1. Сколько книг вышло после 1 января 2000 года?
2. Количество обзоров и средняя оценка для каждой книги.
3. Определить издательство, которое выпустило наибольшее число книг толще 50 страниц — так вы исключите из анализа брошюры.
4. Определить автора с самой высокой средней оценкой книг — учитывайте только книги с 50 и более оценками.
5. Посчитать среднее количество обзоров от пользователей, которые поставили больше 50 оценок.




