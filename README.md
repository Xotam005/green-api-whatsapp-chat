# GREEN-API WhatsApp Chat

Тестовый React-проект на GREEN-API для WhatsApp.

Приложение позволяет:

- ввести `apiUrl`, `idInstance` и `apiTokenInstance`;
- проверить номер через `CheckWhatsapp`;
- получить `chatId`;
- отправить текстовое сообщение через `SendMessage`;
- получать входящие уведомления через `ReceiveNotification`;
- удалять обработанные уведомления через `DeleteNotification`;
- показывать входящие и исходящие сообщения в интерфейсе чата.

## Технологии

- React
- Vite
- JavaScript
- CSS
- Fetch API

## Перед запуском

Инстанс WhatsApp в GREEN-API должен быть **авторизован**.  
В личном кабинете GREEN-API откройте инстанс и подключите WhatsApp по QR-коду или доступному способу авторизации.

## Локальный запуск

```bash
npm install
npm run dev
```

После запуска Vite покажет локальный адрес, обычно:

```text
http://localhost:5173
```

## Данные для входа

Берутся из страницы инстанса GREEN-API:

- `apiUrl`
- `idInstance`
- `apiTokenInstance`

## Использование

1. Авторизуйте WhatsApp-инстанс в GREEN-API.
2. В приложении введите данные инстанса.
3. Введите номер получателя в международном формате без `+`, например `998901234567`.
4. Нажмите **Создать чат**.
5. Приложение вызовет `CheckWhatsapp` и получит `chatId`.
6. Отправьте текстовое сообщение.
7. Входящие сообщения будут получаться через HTTP API.

## HTTP API

Используются методы:

- `CheckWhatsapp`
- `SendMessage`
- `ReceiveNotification`
- `DeleteNotification`

Для получения уведомлений через HTTP API `webhookUrl` в настройках инстанса должен быть пустым.
