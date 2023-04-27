## Экспорт статистики по материалам обучения
### Формат ответа
Отчет выгружается в формате **JSON**

### Структура ответа
| Атрибут |Описание| Типы значений |
| -------| ----- | ---- |
| id | ID материала обучения | int |
| name | Наименование материала обучения (в соответствии с текущим языком компании) | string / null|
| type | Тип материала (pdf, scorm, link, html, test, video) | string / null|
| points | Максимальное количество баллов за прохождение материала (если по типу материала не предусмотрено баллы, то значение null) | int / null |
| statistics | Структура статистики по материалу обучения | array |

### Структура статистики по материалу обучения (атрибут statistics)
| Атрибут |Описание| Типы значений |
| -------| ----- | ---- |
| login | Наименование учетной записи пользователя | string |
| user_status | Статус учетной записи пользователя (active, blocked) | string |
| material_status | Статус учетной записи по материалу обучения (appointed, in_progress, completed, checking, fail) | string |
| points | Количество набранных баллов по материалу обучения | int / null |
| progress | Прогресс пользователя по материалу обучения | int |
| start_at | Дата начала пользователем материала обучения. Формат значения Y-m-d\TH:i:sP (например, 2020-12-01T15:52:01+03:00) | string / null |
| end_at | Дата окончания пользователем материала обучения. Формат значения Y-m-d\TH:i:sP (наприме, 2020-12-01T15:52:01+03:00) |  string / null |
| update_at | Дата последней активности пользователя по материалу обучения. Формат значения Y-m-d\TH:i:sP (наприме, 2020-12-01T15:52:01+03:00) |  string / null |
### [Пример ошибки для параллельного запуска задач одного типа](https://github.com/ekvio-dev/integration-api-response-examples/blob/master/examples/v2/uniq_task_error.json)
### [Пример ошибки недоступности модуля](https://github.com/ekvio-dev/integration-api-response-examples/blob/master/examples/v2/module_unavalible_error.json)
### Пример
[Пример отчета](https://github.com/ekvio-dev/integration-api-response-examples/blob/master/examples/v2/learning-program/materials_statistic.json)