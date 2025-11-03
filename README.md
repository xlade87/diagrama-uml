# Diagrama de Casos de Uso – Gestión de Sistema Escolar

Este es mi segundo intento del diagrama de casos de uso, corregido según las indicaciones siguiendo el ejemplo del tutorial de Solvetic.

## El diagrama incluye:

- Un **sistema** llamado “Gestión de sistema escolar”, representado como un rectángulo.
- **Casos de uso** dentro del sistema, mostrados como óvalos:  
  (Solicitar préstamo, Buscar Libro, Devolver libro, Iniciar sesión, Registrar préstamo, Gestionar catálogo de libros).
- **Actores externos** (los “muñequitos”) fuera del sistema:
  - A la **izquierda**: Estudiante y Bibliotecario.
  - A la **derecha**: Coordinador de biblioteca y Jefe de biblioteca.
- **Relaciones `<<include>>`** entre casos de uso (líneas punteadas con flecha abierta), como:
  - *Buscar Libro* incluye *Solicitar préstamo*.
  - *Iniciar sesión* incluye *Registrar préstamo*.

## Cumplimiento de requisitos técnicos

Aunque no se ven como rectángulos en el diagrama, el sistema está dividido en dos módulos lógicos:
1. **Módulo de Autenticación**: maneja el acceso mediante *Iniciar sesión*.
2. **Módulo de Operaciones Bibliotecarias**: maneja todo lo relacionado con préstamos y catálogo.

Estos módulos están integrados porque solo usuarios autenticados pueden usar las funciones del sistema, y algunos casos de uso dependen de otros (gracias a `<<include>>`).
