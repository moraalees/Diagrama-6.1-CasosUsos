# Diagrama-6.1-CasosUsos

1. Crea el diagrama de uso haciendo uso de platuml, representado los actores y casos de uso que identifiques en los requisitos.
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
