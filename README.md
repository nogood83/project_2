# Проект: Статистический анализ данных

## Описание проекта
Вы аналитик популярного сервиса аренды самокатов GoFast. Вам передали данные о некоторых пользователях из нескольких городов, а также об их поездках. Ваша задача — проанализировать данные и проверить гипотезы, которые могут помочь бизнесу вырасти.

## Описание сервиса GoFast
Пользователи арендуют самокаты через мобильное приложение. Сервис предлагает два варианта использования:

1. **Без подписки**  
   - Абонентская плата отсутствует.  
   - Стоимость одной минуты поездки — 8 рублей.  
   - Стоимость старта (начала поездки) — 50 рублей.  

2. **С подпиской Ultra**  
   - Абонентская плата — 199 рублей в месяц.  
   - Стоимость одной минуты поездки — 6 рублей.  
   - Стоимость старта — бесплатно.  

## Данные
### Основные датасеты
1. **Пользователи** — `users_go.csv`  
   - `user_id` — уникальный идентификатор пользователя.  
   - `name` — имя пользователя.  
   - `age` — возраст.  
   - `city` — город.  
   - `subscription_type` — тип подписки (free, ultra).  

2. **Поездки** — `rides_go.csv`  
   - `user_id` — уникальный идентификатор пользователя.  
   - `distance` — расстояние поездки (м).  
   - `duration` — продолжительность поездки (мин.).  
   - `date` — дата поездки.  

3. **Подписки** — `subscriptions_go.csv`  
   - `subscription_type` — тип подписки.  
   - `minute_price` — стоимость одной минуты.  
   - `start_ride_price` — стоимость начала поездки.  
   - `subscription_fee` — ежемесячная плата.  

## Этапы анализа
### 1. Загрузка данных
- Чтение CSV-файлов с помощью pandas.  
- Вывод первых строк и общей информации о датасетах.  

### 2. Предобработка данных
- Приведение `date` к типу `datetime`.  
- Создание нового столбца с номером месяца.  
- Проверка и обработка пропущенных значений и дубликатов.  

### 3. Исследовательский анализ данных
- Частота встречаемости городов.  
- Соотношение пользователей с подпиской и без.  
- Возраст пользователей.  
- Анализ расстояний и длительности поездок.  

### 4. Объединение данных
- Слияние данных о пользователях, поездках и подписках.  
- Разделение на две группы: с подпиской и без.  
- Визуализация характеристик поездок для обеих групп.  

### 5. Подсчёт выручки
- Агрегация данных по пользователям и месяцам.  
- Рассчёт помесячной выручки с учётом тарифов.  
- Округление длительности поездок до целого.  

### 6. Проверка гипотез
1. Тратят ли подписчики больше времени на поездки?  
2. Превышает ли среднее расстояние одной поездки у подписчиков 3130 метров?  
3. Выше ли помесячная выручка от подписчиков по сравнению с пользователями без подписки?  
4. Снизилось ли количество обращений в техподдержку после обновления серверов?  

## Используемые технологии
- **Python**: pandas, matplotlib, seaborn, scipy.  
- **Jupyter Notebook**: анализ и визуализация данных. 
