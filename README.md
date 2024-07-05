import discord
from discord.ext import commands
import os, random

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='$', intents=discord.Intents.default())

facts = ['При запуске высокотехнологичных ракет в атмосферу выбрасывается огромное количество вредных веществ.','Производство и утилизация аккумуляторов для экологичных беспилотных автомобилей- совсем не экологичные процессы...','В Тихом океане есть мусорное пятно, площадь которого достигает 1,5 млн км²,что больше площади большинства стран мира.Течения сносят сюда миллионы тонн мусора ежегодно, и он превратился в подобие мусорного континента.','Таяние ледников в 2024 году Кажется, что таяние ледников происходит где-то на краю Земли и поэтому не касается нас напрямую. Однако нужно помнить, что этот процесс необратим и его последствия могут быть катастрофическими для человечества. ','Практически вся техника производится из пластика, разложение которого требует сотни лет!']

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')
#     
# @bot.command()
# async def mem(ctx):
#     img_name = random.choice(os.listdir('images'))
#     with open(f'images/{img_name}', 'rb') as f:
#         picture = discord.File(f)
#     await ctx.send(file=picture)
    
@bot.command()
async def fact(ctx):
    await ctx.send('При запуске высокотехнологичных ракет в атмосферу выбрасывается огромное количество вредных веществ.')
    
@bot.command()
async def fact2(ctx):
    await ctx.send('Производство и утилизация аккумуляторов для экологичных беспилотных автомобилей- совсем не экологичные процессы...')
    
@bot.command()   
async def fact3(ctx):
    await ctx.send(' В Тихом океане есть мусорное пятно, площадь которого достигает 1,5 млн км²,что больше площади большинства стран мира.Течения сносят сюда миллионы тонн мусора ежегодно, и он превратился в подобие мусорного континента.')
    
@bot.command()
async def fact4(ctx):
    await ctx.send('Таяние ледников в 2024 году Кажется, что таяние ледников происходит где-то на краю Земли и поэтому не касается нас напрямую. Однако нужно помнить, что этот процесс необратим и его последствия могут быть катастрофическими для человечества. ')
 
@bot.command()
async def fact5(ctx):
    await ctx.send('Практически вся техника производится из пластика, разложение которого требует сотни лет!')
    

@bot.command()
async def random_fact(ctx):
    await ctx.send(random.choice(facts))
 
bot.run('MTI1MTA1NjcyOTk5MTU0NDg3Mw.Gryuo-.GLcug7v-mgAsyVI25xARh2LPkoMG104kbMrqTs')

