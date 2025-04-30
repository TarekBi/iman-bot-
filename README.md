from telegram import Bot, Update
from telegram.ext import CommandHandler, MessageHandler, Filters, Updater

TOKEN = 'توكن_البوت_هون'  # استبدلي بـ التوكن الخاص بك

def start(update, context):
    update.message.reply_text('أهلاً! أنا بوت التحليل.')

updater = Updater(TOKEN, use_context=True)
dp = updater.dispatcher
dp.add_handler(CommandHandler('start', start))

updater.start_polling()
updater.idle()python-telegram-bot==13.15#!/bin/bash
python3 main.py
