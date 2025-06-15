# save_the_earth_bot
import telebot
from config import token

bot = telebot.TeleBot(token)


@bot.message_handler(commands=['start'])
def send_welcome(message):
    bot.reply_to(message, "Привет! Я твой Telegram бот, который поможет тебе спасти нашу планету")

@bot.message_handler(commands=['ideas'])
def send_welcome(message):
    bot.reply_to(message, "Вот идея, как можно спасти планету: сортируй мусор! Клади пластик в один пакет, еду в другой пакет, в третий пакет клади бумагу и картон, а всё остальное складывай в другой пакет. А чтобы не путаться в пакетах, сделай так, чтобы они были в разных цветах!")

bot.polling()
