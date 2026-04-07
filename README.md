# GREEN-API Test Page


Веб-интерфейс для тестирования методов [GREEN-API](https://green-api.com/) — WhatsApp HTTP API.

## Демо

**[https://mikhailbelikov.github.io/green-api-test/](https://mikhailbelikov.github.io/green-api-test/)**

## Реализованные методы

| Метод | Тип | Описание |
|-------|-----|----------|
| `getSettings` | GET | Получение текущих настроек инстанса |
| `getStateInstance` | GET | Получение состояния инстанса |
| `sendMessage` | POST | Отправка текстового сообщения |
| `sendFileByUrl` | POST | Отправка файла по ссылке |

## Как использовать

1. Зарегистрируйтесь в [личном кабинете GREEN-API](https://console.green-api.com/)
2. Создайте инстанс на бесплатном тарифе разработчика
3. Отсканируйте QR-код в WhatsApp → Связанные устройства
4. Скопируйте `idInstance` и `ApiTokenInstance` из личного кабинета
5. Вставьте параметры на странице и вызывайте методы

## CI/CD

Проект использует GitHub Actions для автоматизации:

```
push / PR в main → HTML Lint (HTMLHint) → Deploy на GitHub Pages
```

- Pull Request запускает только линтинг
- Push в `main` запускает линтинг + автодеплой

## Структура проекта

```
green-api-test/
├── index.html                    # Основная страница
├── .github/
│   └── workflows/
│       └── deploy.yml            # CI/CD pipeline
├── .htmlhintrc                   # Конфигурация линтера
├── .gitignore
└── README.md
```

## Локальный запуск

```bash
# Просто откройте в браузере
open index.html
```
