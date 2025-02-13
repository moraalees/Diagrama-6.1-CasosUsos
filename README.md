# Diagrama-6.1-CasosUsos

***1. Crea el diagrama de uso haciendo uso de platuml, representado los actores y casos de uso que identifiques en los requisitos.***
```
@startuml
actor Cliente
actor Banco
rectangle "Cajero automático" {
  usecase "Validarse en el sistema" as R1
  usecase "Sacar dinero" as R2
  usecase "Verificar saldo" as R2_1
  usecase "Verificar límite diario" as R2_2
  usecase "Realizar transferencia" as R4
  usecase "Realizar ingreso" as R5
}

Cliente -> R1
Cliente -> R2
R2 --> R2_1 : «include»
R2 --> R2_2 : «include»
Cliente -> R4
Cliente -> R5
R4 -> Banco
R5 -> Banco
@enduml

```

***2. Describe, haciendo uso de la plantilla, al menos el caso de uso "Sacar dinero", con las interacciones que tiene entre el actor y el caso de uso.***

*Caso de Uso: Sacar Dinero*

Cuando un cliente quiere retirar dinero de su cuenta por el cajero automático, primero debe autenticarse en el sistema. Cuando lo haya hecho, puede sacar dinero e introduce la cantidad deseada. El sistema por defecto comprueba si la cantidad introducida no es mayor que el saldo que hay en ese momento en la cuenta, además de comprobar el límite diario de retiro.

Si ambas condiciones se cumplen, el cajero procede a entregar el dinero y actualiza el saldo en la cuenta, restando la cantidad sacada. Sin embargo, si el saldo es insuficiente o la cantidad deseada es mayor que el límite diario, el sistema muestra un mensaje de error y solicita un nuevo ingreso con una nueva cantidad. Finalmente, cada transacción queda registrada en el sistema para controlar las operaciones realizadas en la cuenta.

***3. Responde a las siguiente pregunta:¿Para qué me sirve tener/realizar un diagrama de casos de uso modelando el sistema que se representa? ¿Qué aporta?***

*¿Para qué sirve?*

Los diagramas de casos de uso sirven para representar el comportamiento de un sistema desde la perspectiva del usuario. Este, permite representar gráficamente las interacciones entre los actores y las funcionalidades que ofrece el sistema, así, ayuda a comprender algún problema o situación en el sistema.

*¿Qué aporta?*

· Claridad en los requisitos: Facilita la visualización de las funcionalidades del sistema de manera sencilla.

· Comunicación efectiva: Mejora el entendimiento entre analistas, desarrolladores y usuarios finales.

· Identificación de actores y relaciones: Define con precisión quién interactúa con el sistema y de qué manera.

· Base para el diseño y desarrollo: Proporciona un punto de partida para la implementación y validación de requerimientos.

· Reducción de errores: Ayuda a evitar omisiones en la planificación del sistema al anticipar posibles escenarios.
