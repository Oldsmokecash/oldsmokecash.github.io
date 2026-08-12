# Web App — TADS реклама + коины

Telegram Mini App для показа рекламы через [TADS](https://tads.me) с начислением коинов пользователям.

## Настройка

1. Зарегистрируйтесь на [tads.me](https://tads.me/register)
2. Добавьте сайт (URL этого GitHub Pages)
3. Создайте два виджета:
   - **TGB** (Text-Graphic Block) — rewarded, клик = награда
   - **Fullscreen** — rewarded, просмотр = награда
4. Скопируйте Widget IDs из дашборда
5. Замените в `index.html`:
   - `YOUR_TGB_WIDGET_ID` → ваш TGB widget ID
   - `YOUR_FULLSCREEN_WIDGET_ID` → ваш Fullscreen widget ID

## Webhook URL

При создании виджета укажите webhook URL:
```
https://YOUR_BOT_SERVER:8080/tads/webhook
```

TADS будет отправлять POST `{"telegram_id": "...", "widget_id": "..."}` при клике/просмотре.

## Награды

- Клик по TGB рекламе: **5 коинов**
- Просмотр Fullscreen: **25 коинов**

## Deploy

```bash
git add .
git commit -m "web app for TADS ads"
git push
```

GitHub Pages автоматически опубликует сайт по адресу:
```
https://oldsmokecash.github.io/web-app/
```
