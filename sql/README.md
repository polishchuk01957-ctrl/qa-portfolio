# SQL Practice

## Про цей розділ

У цьому розділі зібрані SQL-запити, які я виконував під час навчання

Я практикував вибірку даних, фільтрацію, сортування, підрахунок записів та роботу з двома таблицями

## Навчальні таблиці

Для практики я використовував дві таблиці: `patients` та `med_area`

**Таблиця patients**

| id | name | age | med_area_id |
|---:|---|---:|---:|
| 1 | Alex | 25 | 1 |
| 2 | Maria | 34 | 2 |
| 3 | Ivan | 19 | 1 |
| 4 | Anna | 42 | 3 |
| 5 | Oleg | 34 | 2 |

**Таблиця med_area**

| id | area_name |
|---:|---|
| 1 | Cardiology |
| 2 | Neurology |
| 3 | Surgery |
| 4 | Dentistry |

## 1. Вибірка, фільтрація та сортування

### Завдання
Знайти пацієнтів віком понад 30 років і відсортувати їх за віком від меншого до більшого

```sql
SELECT *
FROM patients
WHERE age > 30
ORDER BY age ASC;
```

- `SELECT` — вибирає дані
- `WHERE` — залишає записи, які відповідають умові
- `ORDER BY` — сортує результат

## 2. Підрахунок записів

### Завдання
Порахувати кількість пацієнтів у кожному відділенні

```sql
SELECT med_area_id, COUNT(*) AS total
FROM patients
GROUP BY med_area_id;
```

- `COUNT(*)` — рахує записи
- `GROUP BY` — об'єднує записи з однаковим значенням для підрахунку

## 3. Використання HAVING

### Завдання
Знайти відділення, у яких більше одного пацієнта

```sql
SELECT med_area_id, COUNT(*) AS total
FROM patients
GROUP BY med_area_id
HAVING COUNT(*) > 1;
```

`HAVING` дозволяє залишити тільки ті групи, які відповідають умові

## 4. Об'єднання таблиць за допомогою INNER JOIN

### Завдання
Вивести імена пацієнтів, назви їхніх відділень та вік. Знайти пацієнтів старше 25 років і відсортувати результат від старшого до молодшого

```sql
SELECT med_area.area_name, patients.name, patients.age
FROM patients
JOIN med_area
    ON patients.med_area_id = med_area.id
WHERE patients.age > 25
ORDER BY patients.age DESC;
```

`JOIN` дозволяє отримати дані з двох пов'язаних таблиць

## 5. Використання LEFT JOIN

### Завдання
Вивести всі відділення та кількість пацієнтів у кожному з них, включно з відділеннями без пацієнтів

```sql
SELECT med_area.area_name, COUNT(patients.id) AS patients_count
FROM med_area
LEFT JOIN patients
    ON patients.med_area_id = med_area.id
GROUP BY med_area.area_name;
```

`LEFT JOIN` дозволяє показати всі відділення, навіть якщо пацієнтів у деяких із них немає

`COUNT(patients.id)` рахує тільки тих пацієнтів, для яких знайдено запис

## 6. Пошук відділень без пацієнтів

### Завдання
Знайти відділення, у яких немає пацієнтів

```sql
SELECT med_area.area_name
FROM med_area
LEFT JOIN patients
    ON patients.med_area_id = med_area.id
WHERE patients.id IS NULL;
```

`IS NULL` допомагає знайти записи, для яких не знайдено відповідних даних у таблиці пацієнтів

## Висновок

Під час практики я навчився вибирати, фільтрувати та сортувати дані, рахувати записи й об'єднувати таблиці за допомогою SQL
