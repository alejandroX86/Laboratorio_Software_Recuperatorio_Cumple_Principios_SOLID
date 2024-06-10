README.md

Catedra: Laboratorio de Software
Profesor:Daniel Alejandro Fernandez
Alumno:Omar Alejandro Bazar


Proyecto: Taller de Mantenimiento (Refactorizado)
Este proyecto cumple con los 5 principios SOLID de la siguiente manera:

1. Principio de Responsabilidad Única (Single Responsibility Principle)
Cada clase tiene una única responsabilidad:

MantenimientoManager: Realizar el mantenimiento.
FacturacionManager: Enviar facturas.
InventarioManager: Gestionar el inventario.
Automovil y Camion: Representar vehículos.
Mecanico: Agrupar las responsabilidades de un mecánico.
2. Principio de Abierto/Cerrado (Open/Closed Principle)
La interfaz IVehiculo permite agregar nuevos tipos de vehículos (como Motocicleta, Bicicleta, etc.) sin modificar el código existente. Además, la interfaz IMotor permite agregar nuevos tipos de motores (como MotorDiesel, MotorHibrido, etc.) sin modificar el código existente.

3. Principio de Segregación de Interfaces (Interface Segregation Principle)
Las interfaces ITrabajo, IComida e ICapacitacion segregan correctamente las responsabilidades del mecánico. Cada clase cliente solo implementa las interfaces que necesita.

4. Principio de Sustitución de Liskov (Liskov Substitution Principle)
Las clases Automovil y Camion heredan de la clase base VehiculoBase y pueden ser sustituidas correctamente, ya que implementan los mismos métodos (CalcularRendimientoCombustible y MostrarDetalles) de manera adecuada.

5. Principio de Inversión de Dependencias (Dependency Inversion Principle)
La clase Taller depende de la abstracción IVehiculo en lugar de clases concretas, lo que facilita el mantenimiento y la extensibilidad del código. Además, las clases Automovil y Camion dependen de la abstracción IMotor en lugar de una implementación concreta, lo que también promueve la flexibilidad.

Al seguir estos principios, el código se vuelve más modular, mantenible y extensible. Además, se facilita la reutilización de código y se reduce el acoplamiento entre las clases.
