import random
print("Olá, esse é o nosso Jokenpo, tenha um bom jogo!!")
Modos = input("Escolha o modo de jogo (1 para humano x humano, 2 para humano x
computador, 3 para computador x computador): ")
while Modos not in ["1", "2", "3"]:
print("Modo inválido. Escolha 1, 2 ou 3.")
modalidade = input("Escolha o modo de jogo (1 para humano x humano, 2 para
humano x computador, 3 para computador x computador): ")
score_jogador1 = 0
score_jogador2 = 0
continuar = True
while continuar:
if Modos == "1":
jogada1 = input("Jogador 1, escolha sua jogada (pedra, papel ou tesoura):
")
jogada2 = input("Jogador 2, escolha sua jogada (pedra, papel ou tesoura):
")
elif Modos == "2":
jogada1 = input("Jogador 1, escolha sua jogada (pedra, papel ou tesoura):
")
jogada2 = random.choice(["pedra", "papel", "tesoura"])
print("Jogada do Computador: [jogada2]")
else:
jogada1 = random.choice(["pedra", "papel", "tesoura"])
jogada2 = random.choice(["pedra", "papel", "tesoura"])
if jogada1 == jogada2:
resultado = "Empate"
else:
if (jogada1 == "pedra" and jogada2 == "tesoura"):
resultado = "Jogador 1"
elif (jogada1 == "tesoura" and jogada2 == "papel"):
resultado = "Jogador 1"
elif (jogada1 == "papel" and jogada2 == "pedra"):
resultado = "Jogador 1"
else:
resultado = "Jogador 2"
print(f"Jogador 1 jogou {jogada1}")
print(f"Jogador 2 jogou {jogada2}")
print(f"Resultado: {resultado}")
if resultado == "Jogador 1":
score_jogador1 += 1
elif resultado == "Jogador 2":
score_jogador2 += 1
print(f"Placar: Jogador 1 ({score_jogador1}) - Jogador 2 ({score_jogador2})")
continuar = input("Deseja continuar jogando? (s para continuar, n para sair):
")
if continuar != "s":
continuar = False
