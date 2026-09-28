Markdown
# TPC2: Jogo "Adivinha o número"

## Autor
**Nome:** David Lopes
**Número:** A115067

## Resumo
Este trabalho consiste no desenvolvimento de um programa em Python que implementa o jogo "Adivinha o número". 
O computador gera um número aleatório entre 1 e 100 utilizando a biblioteca `random`. O utilizador tenta adivinhar o número, recebendo dicas textuais indicando se o valor pensado é "Maior" ou "Menor". 
No final, o programa termina informando o número total de tentativas que foram necessárias para acertar.

## Lista de Resultados

print("Adivinha o Número"! Vou pensar num número entre 1 e 100.")
print("O seu objetivo é adivinhar o número em que eu estou a pensar! Vou responder apenas com 'maior', 'menor' ou 'igual'.")

import random
número = random.randint(1, 100)
tentativa = 0
tentativas = 0
while tentativa != número:
    tentativa = int(input("Adivinhe o número "))
    tentativas = tentativas + 1
    if tentativa < número:
        print("Maior!")
    elif tentativa > número:
        print("Menor!")
    else:
        print(f"Acertou em {tentativas} tentativas!")

## Lista de resultados parte 2

print("Adivinha o Número\"! Pense num número entre 1 e 100.")
print("Responda com 'maior', 'menor' ou 'igual'.")

inferior = 1
superior = 100
tentativa = (inferior + superior) // 2

resposta = ""
tentativas = 0

while resposta != "igual":
    print(f"O número em que pensou é maior, menor ou igual a {tentativa}?")
    resposta = input()
    tentativas = tentativas + 1

    if resposta == "maior":
        inferior = tentativa + 1
    elif resposta == "menor":
        superior = tentativa - 1
    elif resposta == "igual":
        print(f"Adivinhei! O número em que pensou é {tentativa}!")
        print(f"Precisei de {tentativas} tentativas para acertar!")
    else:
        print("Resposta inválida! Por favor responda 'maior', 'menor' ou 'igual'.")
        tentativas = tentativas - 1

    tentativa = (inferior + superior) // 2
