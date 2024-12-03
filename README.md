# 2425 - Programación Orientada a Objetos (UEA-L-UFB-030)

Este repositorio contiene el código fuente desarrollado durante la asignatura **Programación Orientada a Objetos**, impartida en la **Universidad Estatal Amazónica**. Está diseñado como un recurso de apoyo para estudiantes y profesionales interesados en conceptos y prácticas de programación orientada a objetos.

## Información de la asignatura

- **Institución**: Universidad Estatal Amazónica (UEA)  
- **Carrera**: Ingeniería en Tecnologías de la Información y Comunicación  
- **Asignatura**: Programación Orientada a Objetos (UEA-L-UFB-030)  
- **Estuidante**: Wilton Stiwar salazar bisbicuz 

## Contenido del repositorio

Este repositorio incluye:
1. Ejercicios prácticos de programación orientada a objetos.
class Persona:
    def __init__(self, nombre, edad, direccion):
        self.nombre = nombre
        self.edad = edad
        self.direccion = direccion

    def mostrar_info(self):
        print(f"Nombre: {self.nombre}")
        print(f"Edad: {self.edad}")
        print(f"Dirección: {self.direccion}")
2. Ejercicio Herencia y Polimorfismoclass Empleado(Persona):
    def __init__(self, nombre, edad, direccion, salario):
        super().__init__(nombre, edad, direccion)
        self.salario = salario

    def mostrar_info(self):
        super().mostrar_info()  # Llamada al método de la clase base
        print(f"Salario: {self.salario}")

# Creación de un objeto de la clase Empleado
empleado1 = Empleado("Wilton Salazar", 20, "Quito", 1500)
empleado1.mostrar_info()

# Creación de un objeto de la clase Persona
persona1 = Persona("Wilton Salazar", 21, "Amazónica")
persona1.mostrar_info()
from abc import ABC, abstractmethod
import math

class Figura(ABC):
    @abstractmethod
    def area(self):
        pass

class Circulo(Figura):
    def __init__(self, radio):
        self.radio = radio

    def area(self):
        return math.pi * self.radio ** 2

class Rectangulo(Figura):
    def __init__(self, largo, ancho):
        self.largo = largo
        self.ancho = ancho

    def area(self):
        return self.largo * self.ancho

# Creación de objetos de las clases derivadas
circulo = Circulo(5)
rectangulo = Rectangulo(10, 4)

print(f"Área del círculo: {circulo.area()}")
print(f"Área del rectángulo: {rectangulo.area()}")
class Vehiculo:
    numero_de_ruedas = 4  # Atributo de clase

    def __init__(self, marca, modelo):
        self.marca = marca  # Atributo de instancia
        self.modelo = modelo  # Atributo de instancia

    @classmethod
    def mostrar_ruedas(cls):
        print(f"El vehículo tiene {cls.numero_de_ruedas} ruedas.")

    def mostrar_info(self):
        print(f"Marca: {self.marca}, Modelo: {self.modelo}")

# Creación de un objeto de la clase Vehiculo
vehiculo1 = Vehiculo("Toyota", "Corolla")
vehiculo1.mostrar_info()
vehiculo1.mostrar_ruedas()
