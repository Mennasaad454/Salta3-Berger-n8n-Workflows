# Salta3-Berger-n8n-Workflows

A collection of automation workflows for a fictional restaurant called **Salta3 Berger**. Built using [n8n](https://n8n.io) to streamline operations like staff task management, inventory updates, and sales reporting.

---

## About Salta3 Berger

**Salta3 Berger** is a fast-food restaurant run by:
- **Salta3** — Manager
- **Shafeeq** — Cashier
- **Sponge** — Chef

This repo documents automation workflows designed to simplify their daily operations.

---

## 📊 Workflows Overview

| Workflow File                          | Description                                                             | Tools Used              |
|:--------------------------------------|:------------------------------------------------------------------------|:------------------------|
| `shafeeq_daily_tasks.json`             | Manager Salta3 writes Shafeeq’s daily tasks into a Google Sheet; sends them via email every morning at 8 AM. | Schedule Trigger, Google Sheets, Gmail API |
| `order_submission_and_notification.json` | When Shafeeq takes an order through a form, it’s added to a Google Sheet and emailed to Sponge to start cooking. | On form Trigger, Google Sheets, Gmail API |
| `salta3_stock_management.json`        | Shafeeq reports stock updates via Telegram; it updates the stock Google Sheet and sends a confirmation message back. | Telegram API, Google Sheets |
| `salta3_order_management.json`        | Shafeeq fills out an order form; the order is sent to Sponge via Telegram, added to `Salta3 Orders` Google Sheet, and updates the last order number. | Telegram API, Google Sheets |
| `kitchen_response_system.json`        | Sponge updates an order’s status via Telegram. If marked “Done”, it updates the Google Sheet and subtracts used ingredients from stock. | Code node, Telegram API, Google Sheets |
| `AI_Telegram_Bot.json`                | AI-powered Telegram assistant that responds to customer inquiries about the menu, takes burger orders, confirms details, and logs orders to Google Sheets. | Telegram API, OpenAI GPT-4, Google Sheets |
---
