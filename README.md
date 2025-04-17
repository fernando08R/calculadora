# calculadora
def sumar(a, b):
    return a + b

def restar(a, b):
    return a - b

def multiplicar(a, b):
    return a * b

def dividir(a, b):
    if b == 0:
        return "Error: No se puede dividir por cero."
    return a / b

def main():
    print("=== Calculadora Básica ===")
    print("Operaciones disponibles:")
    print("1. Sumar")
    print("2. Restar")
    print("3. Multiplicar")
    print("4. Dividir")

    opcion = input("Elige una opción (1/2/3/4): ")

    try:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))
    except ValueError:
        print("Error: Debes ingresar números válidos.")
        return

    if opcion == '1':
        resultado = sumar(num1, num2)
        operacion = "suma"
    elif opcion == '2':
        resultado = restar(num1, num2)
        operacion = "resta"
    elif opcion == '3':
        resultado = multiplicar(num1, num2)
        operacion = "multiplicación"
    elif opcion == '4':
        resultado = dividir(num1, num2)
        operacion = "división"
    else:
        print("Opción no válida.")
        return

    print(f"El resultado de la {operacion} es: {resultado}")

if __name__ == "__main__":
    main()
