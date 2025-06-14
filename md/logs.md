# 📄 Logs  {#logs}

## 📌 Назначение листа

Лист служит для **автоматического логирования событий, действий и изменений**, происходящих в документе.  
Записи позволяют:
- отслеживать активность пользователей,
- выявлять ошибки или отклонения в поведении системы,
- оптимизировать алгоритмы,
- обеспечивать прозрачность взаимодействий.

---

## 📝 Структура таблицы

| Столбец | Назначение |
|--------|------------|
| A      | **№** по порядку (добавляется автоматически) |
| B      | **Дата** — в формате `ГГГГ-MM-ДД` |
| C      | **Время** — в формате `чч:мм:сс` |
| D      | **Роль пользователя** — например: `"Педагог"`, `"Админ"` |
| E      | **Имя пользователя** — определяется на основе листа **🛠️ Legend (list-script)** |
| F      | **Email** пользователя |
| G      | **Тип действия** — например: `"Редактирование"`, `"Уведомление"`, `"Копирование списка"` |
| H      | **Сообщение или комментарий** |
| I      | **Название листа**, где произошло действие |
| J      | **Ячейка**, к которой относится действие (если применимо) |
| K      | **Новое значение** — если действие связано с изменением содержимого ячейки |

---

## ⚙️ Автоматизация

- Записи в лист **добавляются автоматически** с помощью Apps Script при выполнении различных действий, включая:
  - показ модального окна (например, уведомления о непрочитанных записях),
  - изменение согласия,
  - редактирование информации,
  - экспорт/копирование списков.

---

## ⚠️ Важно

- **Не изменяйте содержимое вручную** — это может нарушить хронологию или структуру логов.
- **Типы действий и сообщения** могут быть расширены/уточнены системным администратором при необходимости.

---

## 👨‍💻 Ответственный

**Системный администратор / разработчик скриптов**  
Следит за корректностью логирования, настройками скриптов и безопасностью изменений.
