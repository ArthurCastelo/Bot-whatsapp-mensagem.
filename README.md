# Bot-whatsapp-mensagem.
Bot de whatsapp para enviar mensagens automatizadas como uma lista de transmissão.


import pywhatkit
import keyboard
from time import sleep
from datetime import datetime

#Deve estar coonectado o seu whatsapp no computador e com conexão estável
#Não deve mexer o mouse, pois irá parar o programa
#Deve botar os números completos com DDD e código postal.

contatos=['+55********','+55********']
while len(contatos)>=1: #Tamanho da lista para não ficar em looping infinito
    pywhatkit.sendwhatmsg(contatos[0],'Olá, voce esta sendo minha cobaia para estudos de chat bot!', datetime.now().hour, datetime.now().minute+1 )
    del contatos[0]
    sleep(30)
    keyboard.press_and_release('ctrl + w')
