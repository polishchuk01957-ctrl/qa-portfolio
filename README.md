QA Portfolio

Вітаю! Я початківець QA Engineer, який вивчає ручне тестування вебзастосунків, тест-дизайн, API testing та SQL

У цьому репозиторії зібрані мої практичні роботи, приклади баг-репортів і результати самостійного навчання

Навички та інструменти

* Manual QA: функціональне та регресійне тестування, тест-дизайн, складання баг-репортів
* Bug Tracking: Jira
* API Testing: Postman, Swagger, HTTP-запити, перевірка статус-кодів і JSON-відповідей
* SQL: SELECT, WHERE, ORDER BY, LIMIT, GROUP BY, HAVING, COUNT, AVG, INNER JOIN, LEFT JOIN

## Практичні роботи

### Bug Reports — PUMA

Під час самостійного тестування інтернет-магазину PUMA було виявлено та задокументовано три дефекти:

1. [Невідповідність локалізації банерів](bug-reports/PUMA-01-localization.md)
2. [Повідомлення про помилку під час введення пароля](bug-reports/PUMA-02-password-validation.md)
3. [Зникнення форми оформлення замовлення](bug-reports/PUMA-03-checkout-city.md)

Кожен звіт містить кроки відтворення, очікуваний і фактичний результати, тестове оточення та скриншоти

### Bug Reports — ROZETKA

Навчальні приклади баг-репортів для практики опису дефектів і визначення Severity та Priority.

1. [Помилка в написанні слова «Сміливість» у хедері](bug-reports/ROZETKA-01-header-typo.md)
2. [Не працює кнопка «Знайти» на головній сторінці](bug-reports/ROZETKA-02-search-button.md)

Описані дефекти є вигаданими навчальними прикладами й не стверджують про наявність реальних проблем на сайті ROZETKA.

### API Testing — Swagger Petstore

Практичні роботи:
- [API-001 — Створення та отримання даних про тварину](api-testing/API-001-create-and-get-pet.md)
- [API-002 — Негативне тестування Swagger Petstore](api-testing/API-002-negative-testing.md)
## Сертифікати

- [SQL — вступний курс](https://stepik.org/cert/3337270)
- [Тестування API за допомогою Postman](https://stepik.org/cert/3342809)
### Test Cases — PUMA

Тест-кейси для перевірки функціональності інтернет-магазину PUMA.

1. [Перевірка локалізації головної сторінки](test-cases/PUMA-TC-001-localization.md)
2. [Перевірка успішної реєстрації користувача](test-cases/PUMA-TC-002-registration.md)
3. [Перевірка валідації пароля](test-cases/PUMA-TC-003-password-validation.md)
4. [Перевірка оформлення замовлення з доставкою до Києва](test-cases/PUMA-TC-004-checkout-kyiv.md)
5. [Перевірка оформлення замовлення з доставкою до Маріуполя](test-cases/PUMA-TC-005-checkout-mariupol.md)

### Test Cases — ROZETKA

Тест-кейси для перевірки пошуку товарів і роботи кошика.

1. [Пошук товару за назвою](test-cases/ROZETKA-TC-001-product-search.md)
2. [Пошук товару, якого немає в каталозі](test-cases/ROZETKA-TC-002-product-search-no-results.md)
3. [Додавання товару до кошика](test-cases/ROZETKA-TC-003-add-product.md)
4. [Зміна кількості товару в кошику](test-cases/ROZETKA-TC-004-change-quantity.md)
5. [Видалення товару з кошика](test-cases/ROZETKA-TC-005-remove-product.md)
6. [Збереження товару в кошику після повторного входу](test-cases/ROZETKA-TC-006-cart-persistence.md)

## Мета

Розвивати практичні навички тестування програмного забезпечення та отримувати перший професійний досвід у сфері QA





