# Руководство пользователя AUNotebot

## 1. Старт
1. Откройте чат с ботом.
2. Отправьте `/start`.
3. На стартовом экране доступны: `Find`, `Tasks`, `Notes`, `Reminders`, `Drafts`, `More`.

## 2. Язык
- Меню: `More -> Settings -> Language`.
- Поддерживаются: English, Русский, Українська, Español, Português, Français.

## 3. Создание заметки или задачи
Заметка - это набор текста; задача - это заметка, которую нужно выполнить (у неё может быть установлен срок исполнения).
1. Отправьте текст/голос/видео/изображение.
2. Бот создаст черновик.
3. Нажмите `📝 Save as Note` для создания заметки или `🟧 Save as Task` для создания задачи.
   Впоследствии можно будет превратить заметку в задачу, нажав на кнопку `⬛ Make Task`.

## 4. Пересылка сообщений
- Несколько пересланных сообщений в одном действии объединяются в один черновик.
- Окно объединения настраивается: `More -> Settings -> Multiple message merge time`.
- Хэштеги в отдельном сообщении добавляются в теги черновика.

## 5. Поиск
- Кнопка `🔎 Find` включает интерактивный режим.
- Отправьте вопрос в свободной форме.
- Бот вернет краткий ответ и список релевантных элементов кнопками.

## 6. Действия в карточке
### Заметка
- `✏️ Edit`, `🏷️ Tags`, `⬛ Make Task`, `❌ Remove`, `⬅️ Back`

### Задача
- `✏️ Edit`, `✅ Done/🔄 Re-do`, `⏰ Reminder`, `🏷️ Tags`, `🔁 Make Note`, `🔀 Merge`, `👥 Assign`, `❌ Remove`, `⬅️ Back`

## 8. Теги и темы
- `Tags` открывает теги элемента.
- По нажатию на тег открывается список связанных элементов.
- В меню темы доступны `Edit` и `Delete`.

## 9. Напоминания
- В задаче нажмите `⏰ Reminder`.
- Введите дату/время в свободной форме (например, «завтра 9:00»).

## 10. Настройки
`More -> Settings`:
- Language
- Timezone
- Mark as done
- Copy text for edits
- Daily task digest
- Evening summary
- Multiple message merge time
- No. of items
- Show bottom menu

## 11. Помощь и правовые документы
- `More -> Help` открывает это руководство в веб-версии.
- `More -> Legal` открывает Terms & Conditions на текущем языке интерфейса.

## 12. Обратная связь
- Идеи и вопросы: `@aunotebot_support`

## Связанные документы
- Terms & Conditions: [Legal docs repository](https://github.com/panslav/aunotebot_public/tree/main/docs/legal)
- Screenflow: [Screenflow](https://github.com/panslav/supernotes/blob/tasked/docs/Screenflow.md)
- Installation: [Installation](https://github.com/panslav/supernotes/blob/tasked/docs/installation.md)
