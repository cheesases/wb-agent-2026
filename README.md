# 🛒 wb-agent-2026

**MCP-сервер для Wildberries** — подключи любого AI-агента (Claude Desktop и другие) к своему магазину на WB.

[![npm version](https://img.shields.io/npm/v/wb-agent-2026)](https://www.npmjs.com/package/wb-agent-2026)
[![license](https://img.shields.io/npm/l/wb-agent-2026)](./LICENSE)

---

## ⚡ Быстрый старт

### 1. Получи токен WB

Зайди в [личный кабинет продавца](https://seller.wildberries.ru/) → **Настройки → Доступ к API** → создай токен.

### 2. Добавь в конфиг Claude Desktop

**Найди файл конфига:**

- **Mac:** `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

**Вставь конфигурацию:**

```json
{
  "mcpServers": {
    "wildberries": {
      "command": "npx",
      "args": ["-y", "wb-agent-2026"],
      "env": {
        "WB_API_TOKEN": "ВАШ_ТОКЕН_ЗДЕСЬ"
      }
    }
  }
}
```

### 3. Перезапусти Claude Desktop

Готово! 🎉 Теперь Claude может работать с твоим магазином на WB.

---

## 🛠 Доступные инструменты

| Инструмент | Описание | Тип |
|---|---|---|
| `get_feedbacks` | Отзывы покупателей | чтение |
| `reply_feedback` | Ответить на отзыв | **запись** |
| `get_unanswered_count` | Кол-во неотвеченных отзывов | чтение |
| `get_stocks` | Остатки на складах | чтение |
| `get_orders` | Последние заказы | чтение |
| `get_sales` | Данные о продажах | чтение |
| `get_nm_report` | Отчёт по товарам (просмотры, корзина, заказы) | чтение |
| `get_advert_list` | Список рекламных кампаний | чтение |
| `get_advert_stats` | Статистика рекламы | чтение |
| `get_prices` | Цены и скидки | чтение |
| `get_seller_info` | Информация о продавце | чтение |
| `get_questions` | Вопросы покупателей | чтение |
| `get_supplies` | Список поставок | чтение |
| `get_financial_report` | Финансовый отчёт | чтение |
| `get_documents` | Финансовые документы | чтение |

---

## 💬 Примеры запросов к Claude

После подключения можно спрашивать Claude:

- _«Покажи мои последние заказы на WB»_
- _«Сколько неотвеченных отзывов у меня есть?»_
- _«Какие остатки на складах?»_
- _«Ответь на все отзывы без ответа»_
- _«Покажи статистику рекламных кампаний»_

---

## ⚙️ Конфигурация

| Переменная | Описание | Обязательно |
|---|---|---|
| `WB_API_TOKEN` | Токен API продавца Wildberries | ✅ Да |

Или передай через CLI:
```bash
npx wb-agent-2026 --token=твой_токен
```

---

## 🔧 Разработка

```bash
git clone https://github.com/cheesases/wb-agent-2026.git
cd wb-agent-2026
npm install
npm run build
```

---

## 👤 Автор

- Telegram: [@khaliullovv](https://t.me/khaliullovv)
- Instagram: [@khaliuloff](https://instagram.com/khaliuloff)

---

## 📄 Лицензия

[MIT](./LICENSE)
