# Programa para calcular el área de un triángulo
# Descripción: Este programa solicita al usuario la base y la altura de un triángulo,
# calcula el área utilizando la fórmula correspondiente y muestra el resultado.
# Se utilizan diferentes tipos de datos e identificadores con convenciones adecuadas.

def calcular_area_triangulo(base: float, altura: float) -> float:
    """
    Calcula el área de un triángulo dados su base y altura.
    Parámetros:
        base (float): La base del triángulo.
        altura (float): La altura del triángulo.
    Retorna:
        float: El área del triángulo.
    """
    area = (base * altura) / 2
    return area

# Solicitar datos al usuario
nombre_usuario = input("Ingrese su nombre: ")  # tipo string
print(f"Hola, {nombre_usuario}!")

base_triangulo = float(input("Ingrese la base del triángulo en cm: "))  # tipo float
altura_triangulo = float(input("Ingrese la altura del triángulo en cm: "))  # tipo float

# Validación simple (boolean)
datos_validos = base_triangulo > 0 and altura_triangulo > 0

if datos_validos:
    resultado_area = calcular_area_triangulo(base_triangulo, altura_triangulo)
    print(f"El área del triángulo es: {resultado_area} cm²")
else:
    print("Error: La base y la altura deben ser mayores a cero.")
