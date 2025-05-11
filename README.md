# -Pares-e-mpares
def identificar_pares_impares(numeros):
    pares = []
    impares = []

    for num in numeros:
        if num % 2 == 0:
            pares.append(num)
        else:
            impares.append(num)

    return pares, impares

def main():
    entrada = input("Digite números separados por vírgula (ex: 1,2,3,4): ")

    try:
        numeros = [int(n.strip()) for n in entrada.split(',')]
        pares, impares = identificar_pares_impares(numeros)

        print("\nResultado:")
        print("Pares:", pares if pares else "Nenhum número par")
        print("Ímpares:", impares if impares else "Nenhum número ímpar")

    except ValueError:
        print("Erro: digite apenas números inteiros separados por vírgulas.")

if __name__ == "__main__":
    main()

Digite números separados por vírgula (ex: 1,2,3,4): 4, 9, 12, 33, 10

Resultado:
Pares: [4, 12, 10]
Ímpares: [9, 33]
