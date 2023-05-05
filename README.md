# trabalho-de-programação 
# professora: Mariana Flavio 
# Alunos: Daniel Macedo e Carlos Alex


# a primeira linha pede ao usuário para digitar uma frase para teste usando a função input().

frase=(input("digite a frase para o teste: "))
print(frase)

# converte a frase digitada para letras minúsculas usando o método lower().

frase = frase.lower()

# cria um dicionário vazio chamado contador 

contador = {}

# calcula o tamanho da frase usando a função len() e armazena esse valor na variável tamanho.

tamanho=len(frase)

# cria uma variável i iniciada com 0.

i = 0

# cria uma variável n com o tamanho da frase

n = len(frase)

# inverte a ordem da frase usando um looping while que adiciona cada letra da frase de trás pra frente na variável invertida.

invertida = ""

while tamanho > 0:
  invertida += frase[tamanho-1]
  tamanho -= 1
print('A frase invertida fica assim: ',invertida)

# conta a quantidade de vezes que cada letra aparece na frase usando outro looping while e adicionando cada letra e sua contagem correspondente ao dicionário contador.

while i < n:
    if frase[i] != ' ':
        if frase[i] not in contador:
            contador[frase[i]] = 1
        else:
            contador[frase[i]] = contador[frase[i]]+ 1
    i = i + 1

# imprime o dicionário contador com as letras e suas contagens correspondentes.

print("contagem de letras na frase:")
for letra, contador in contador.items():
    print(f"{letra}: {contador}")

# pede ao usuário para informar a quantidade de terras repetidas que deseja verificar.

Quant_repetidas= int(input("Diga a quantidade de letras repetidas: "))

# usa um if e um else para verificar se há mais de 3 letras repetidas na frase. Se houver, imprime “há muitas letras repetidas” e se não houver, imprime “há poucas letras repetidas!”

if Quant_repetidas >= 3:
  print("Há muitas letras repetidas!")

else:
  print("Há poucas letras repetidas!")

