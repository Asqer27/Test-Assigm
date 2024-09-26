# Test-Assigm
+----------------------------------+
| Имя: [__________________________] |
| Дата рождения: [______________]  |
| Email: [_______________________] |
| Телефон: [_____________________] |
| Место работы: [______________]   |
| Месячная зарплата: [__________]  |
| Другие задолженности: [______]   |
+----------------------------------+
| [Отправить]                      |
+----------------------------------+

Страница результата (одобрение):
+----------------------------------+
| Ваш займ готов, мы готовы        |
| выдать вам X рублей на 1 год.    |
| Вернуть нужно будет Y рублей!    |
| Для получения денег, пожалуйста, |
| позвоните по телефону [номер].   |
+----------------------------------+
Страница результата (отказ):
+----------------------------------+
| Простите, мы не можем вам помочь |
+----------------------------------+

graph TD;
    A[Сбор данных клиента] --> B{Проверка возраста}
    B -->|< 18 или > 90| C[Отказ]
    B -->|18-90| D{Проверка зарплаты}
    D -->|< 100| C[Отказ]
    D -->|>= 100| E{Проверка занятости}
    E -->|Безработный| C[Отказ]
    E -->|Работает| F[Расчет суммы займа]
    F --> G[Расчет суммы для возврата]
    G --> H[Отправка решения на email]
    G --> I[Отображение результата на странице]

   graph TD;
    A[Сбор данных клиента] --> B{Проверка возраста}
    B -->|< 18 или > 90| C[Отказ]
    B -->|18-90| D{Проверка зарплаты}
    D -->|< 100| C[Отказ]
    D -->|>= 100| E{Проверка занятости}
    E -->|Безработный| C[Отказ]
    E -->|Работает| F[Расчет суммы займа]
    F --> G[Расчет суммы для возврата]
    G --> H[Отправка решения на email]
    G --> I[Отображение результата на странице]

