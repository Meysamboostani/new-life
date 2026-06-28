from telegram import Update
from telegram.ext import Application, CommandHandler, MessageHandler, ContextTypes, filters

BOT_TOKEN = "YOUR_BOT_TOKEN"

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text(
        "Hello! I am your Telegram bot."
    )

async def echo(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text(
        f"You said: {update.message.text}"
    )

app = Application.builder().token(BOT_TOKEN).build()

app.add_handler(CommandHandler("start", start))
app.add_handler(MessageHandler(filters.TEXT & ~filters.COMMAND, echo))

print("Bot is running...")
app.run_polling()
python-telegram-bot==22.1
# Telegram Echo Bot

A simple Telegram bot built with Python.

## Installation

```bash
pip install -r requirements.txt


Move USDC to and from Stellar with CCTP

Unified Balance Kit: Production Safeguards and Recovery Patterns for spend

Transaction memos and batch transactions activate on Arc Testnet

Arc x Uniswap🦄 Swap and liquidity infrastructure for Arc

Event Replay: Privacy on Arc: What Builders Should Know
