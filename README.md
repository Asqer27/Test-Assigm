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

Идеи по улучшению процесса
Улучшение UX/UI:
Добавить валидацию полей ввода на клиентской стороне для предотвращения ошибок ввода.
Использовать автозаполнение и подсказки для полей, таких как дата рождения и место работы.
Дополнительные проверки:
Включить проверку кредитной истории клиента для более точного анализа рисков.
Добавить возможность загрузки документов, подтверждающих доход и занятость.
Персонализация:
Включить возможность настройки процентной ставки в зависимости от кредитной истории и других факторов.
Предоставить клиенту возможность выбора условий займа (например, срок займа, ежемесячные платежи).
Автоматизация:
Интегрировать систему с внешними базами данных для автоматической проверки данных клиента (например, налоговая служба, бюро кредитных историй).
Использовать машинное обучение для улучшения алгоритмов принятия решений на основе исторических данных.
Улучшение коммуникации:
Добавить возможность отправки уведомлений клиенту через SMS или мессенджеры.
Включить чат-бота для поддержки клиентов и ответов на часто задаваемые вопросы.
