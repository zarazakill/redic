# MTProto Proxy — Сайт для клиентов

Статичный сайт на GitHub Pages для раздачи MTProto прокси-ссылок клиентам Telegram.

## Как пользоваться

### 1. Структура ссылки

Сайт принимает параметры через URL:

```
https://YOUR_USERNAME.github.io/YOUR_REPO/?server=СЕРВЕР&port=ПОРТ&secret=СЕКРЕТ&source=МЕТКА&user=ИМЯ
```

| Параметр | Описание | Пример |
|----------|----------|--------|
| `server` | Адрес вашего сервера | `wwcat.duckdns.org` |
| `port` | Порт MTProto прокси | `8043` |
| `secret` | Секрет (dd+32hex для Secure) | `ddb8e96e18d53dfb...` |
| `secret_tls` | TLS-секрет (ee+hex) | `ee...` |
| `source` | **Метка источника** | `website`, `vk_ad`, `private` |
| `user` | Имя клиента (опционально) | `ivan` |

### 2. Примеры ссылок

**Для сайта (общая ссылка):**
```
https://yoursite.github.io/proxy/?server=wwcat.duckdns.org&port=8043&secret=ddb8e96e...&source=website
```

**Персональная ссылка для конкретного клиента:**
```
https://yoursite.github.io/proxy/?server=wwcat.duckdns.org&port=8043&secret=ddb8e96e...&source=ivan_personal&user=ivan
```

**Ссылка из рекламы:**
```
https://yoursite.github.io/proxy/?server=wwcat.duckdns.org&port=8043&secret=ddb8e96e...&source=vk_campaign_2024
```

### 3. Метки источника (`source`)

Метка источника позволяет понять **откуда пришёл клиент**:

- `website` — пришёл с главного сайта
- `telegram_channel` — из Telegram-канала
- `vk_ad` — из рекламы ВКонтакте
- `private_ivan` — персональная ссылка для Ивана
- `qr_code` — отсканировал QR-код

В приложении TorManager в вкладке **"MTProto клиенты"** будет видно поле **"Метка источника"** для каждого подключения.

### 4. Включить GitHub Pages

1. Зайдите в **Settings → Pages** вашего репозитория
2. Source: `Deploy from a branch`
3. Branch: `main`, folder: `/docs`
4. Сохраните

Сайт будет доступен по адресу: `https://USERNAME.github.io/REPO/`

## Структура файлов

```
docs/
  index.html     — главная страница с кнопкой подключения
  README.md      — эта документация
```
