<div align="center">

# Telegram Sales Assistant Bot

</div>

<div align="center">

<table width="100%">
<tr>
<td align="center" width="50%"><b>🇷🇺 Описание</b></td>
<td align="center" width="50%"><b>🇬🇧 Description</b></td>
</tr>
<tr>
<td align="justify" width="50%" style="text-align:justify;">

Этот проект — Telegram-бот для автосалона, который на основе запроса пользователя и CRM-данных предлагает решения или делает апселл с помощью искусственного интеллекта (GPT). Бот сохраняет историю диалога для каждого пользователя и персонализирует ответы на основе информации из CRM.

</td>
<td align="justify" width="50%" style="text-align:justify;">

This project is a Telegram bot for a car dealership. It uses user queries and CRM data to suggest solutions or make upsell offers with the help of AI (GPT). The bot saves each user's chat history and personalizes responses based on CRM data.

</td>
</tr>
</table>

---

<table width="100%">
<tr>
<td align="center" width="50%"><b>🇷🇺 Файлы проекта</b></td>
<td align="center" width="50%"><b>🇬🇧 Project Files</b></td>
</tr>
<tr>
<td align="justify" width="50%" style="text-align:justify;">

- <b>telegram_sales_bot.py</b> — основной код Telegram-бота, интеграция с OpenAI и CRM.
- <b>apikey.py</b> — файл, в котором хранится API-ключ для платформы OpenAI/OpenRouter.
- <b>requirements.txt</b> — список зависимостей для запуска проекта (см. ниже).

</td>
<td align="justify" width="50%" style="text-align:justify;">

- <b>telegram_sales_bot.py</b> — main Telegram bot code, integrates with OpenAI and CRM.
- <b>apikey.py</b> — stores the API key for OpenAI/OpenRouter.
- <b>requirements.txt</b> — dependencies needed to run the project (see below).

</td>
</tr>
</table>

---

<table width="100%">
<tr>
<td align="center" width="50%"><b>🇷🇺 Быстрый старт</b></td>
<td align="center" width="50%"><b>🇬🇧 Quick Start</b></td>
</tr>
<tr>
<td align="justify" width="50%" style="text-align:justify;">

<b>1. Клонируйте репозиторий</b>

```sh
git clone https://github.com/DokiMakuro4ka/TgBot
cd (ваша папка репозитория)
```

<b>2. Установите зависимости</b>

```sh
pip install -r requirements.txt
```

<b>Минимальный requirements.txt:</b>
```
pyTelegramBotAPI
openai
```

<b>3. Настройте ключи</b>

- В файле <code>token_1.py</code> укажите ваш OpenAI API ключ:
  ```python
  API_KEY = "your-openai-api-key"
  ```
- В файле <code>telegram_sales_bot.py</code> укажите токен Telegram-бота:
  ```python
  TG_TOKEN = "your-telegram-bot-token"
  ```

<b>4. Запустите бота</b>

```sh
python tg_bot_ai.py
```

</td>
<td align="justify" width="50%" style="text-align:justify;">

<b>1. Clone the repository</b>

```sh
git clone https://github.com/DokiMakuro4ka/TgBot
cd (your repository folder)
```

<b>2. Install dependencies</b>

```sh
pip install -r requirements.txt
```

<b>Minimal requirements.txt:</b>
```
pyTelegramBotAPI
openai
```

<b>3. Configure keys</b>

- In <code>token_1.py</code>, set your OpenAI API key:
  ```python
  API_KEY = "your-openai-api-key"
  ```
- In <code>telegram_sales_bot.py</code>, set your Telegram bot token:
  ```python
  TG_TOKEN = "your-telegram-bot-token"
  ```

<b>4. Run the bot</b>

```sh
python tg_bot_ai.py
```

</td>
</tr>
</table>

---

<table width="100%">
<tr>
<td align="center" width="50%"><b>🇷🇺 Как работает бот</b></td>
<td align="center" width="50%"><b>🇬🇧 How the bot works</b></td>
</tr>
<tr>
<td align="justify" width="50%" style="text-align:justify;">

- После запуска бот приветствует пользователя и показывает пример CRM-записи.
- Пользователь отправляет любой текст — бот отвечает, учитывая CRM-информацию.
- Для сброса истории диалога используйте команду <b>/reset</b>.
- История диалога хранится для каждого пользователя отдельно (в оперативной памяти).

</td>
<td align="justify" width="50%" style="text-align:justify;">

- After launch, the bot greets the user and shows a sample CRM record.
- The user sends any message — the bot replies, taking CRM information into account.
- Use the <b>/reset</b> command to reset the dialog history.
- Each user's dialog history is stored separately (in memory).

</td>
</tr>
</table>

---

<table width="100%">
<tr>
<td align="center" colspan="2" style="width:100%"><b>🇬🇧 Sample CRM record used in the bot</b></td>
</tr>
<tr>
<td align="left" colspan="2" style="width:100%;text-align:left;">

```python
crm_record = {
    "name": "Alexey",
    "last_purchase": "Audi Q7",
    "budget": 20000000,
    "deal_status": "In progress"
}
```

</td>
</tr>
</table>

---

<table width="100%">
<tr>
<td align="center" width="50%"><b>🇷🇺 Безопасность</b></td>
<td align="center" width="50%"><b>🇬🇧 Security</b></td>
</tr>
<tr>
<td align="justify" width="50%" style="text-align:justify;">

<b>Не публикуйте свои реальные API-ключи и токены Telegram-бота в публичных репозиториях!</b>
- Добавьте файл <code>apikey.py</code> в <code>.gitignore</code> перед публикацией.
- Для продакшена рекомендуется хранить ключи в переменных окружения.

</td>
<td align="justify" width="50%" style="text-align:justify;">

<b>Do not publish your real API keys or Telegram bot tokens in public repositories!</b>
- Add the <code>apikey.py</code> file to <code>.gitignore</code> before publishing.
- For production, it is recommended to store keys in environment variables.

</td>
</tr>
</table>

---

<table width="100%">
<tr>
<td align="center" width="50%"><b>🇷🇺 Возможные доработки</b></td>
<td align="center" width="50%"><b>🇬🇧 Possible Improvements</b></td>
</tr>
<tr>
<td align="justify" width="50%" style="text-align:justify;">

- Получение CRM-данных из реальной базы данных.
- Добавление авторизации пользователей.
- Хранение истории диалогов в базе данных.
- Поддержка мультиязычности.

</td>
<td align="justify" width="50%" style="text-align:justify;">

- Fetch CRM data from a real database.
- Add user authentication.
- Store dialog history in a database.
- Add multilingual support.

</td>
</tr>
</table>

</div>
