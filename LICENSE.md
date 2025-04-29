from telegram import Update
from telegram.ext import CommandHandler, Updater, CallbackContext
import os

# ضعي توكن البوت الحقيقي بدل 'توكن البوت هون'
TOKEN = os.getenv('BOT_TOKEN', 'توكن البوت هون')

def start(update: Update, context: CallbackContext):
    update.message.reply_text('أهلاً إيمان! أنا بوت التحليل الخاص بكِ، كيف يمكنني مساعدتك؟')

updater = Updater(TOKEN, use_context=True)
dp = updater.dispatcher
dp.add_handler(CommandHandler('start', start))

updater.start_polling()
updater.idle()#!/bin/bash
python3 main.pypython-telegram-bot==13.15
