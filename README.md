# Primeiro-c-digo-em-Python
# Aula da Alura 
import requests 


url = "https://raw.githubusercontent.com/guilhermeonrails/api-imersao-ia/main/words.json"
resposta = requests.get(url) 
data = resposta.json() 

import random 

valor_secreto = random.choice(data)  
palavra_secreta = valor_secreto["palavra"] 
dica = valor_secreto["dica"]  
 

print(f" A palavra secreta tem {len(palavra_secreta)} letras")
print (f" a dica é {dica}")
chute = input(f" O que vc acha que é?")
if chute == palavra_secreta:
  print("acertou")

else: 
  print(f'Errooouu.. a palavra secreta era {palavra_secreta}')
  
