# Casos de uso del sistema

Los casos de uso describen la interacción entre los usuarios y las principales funcionalidades del prototipo.

## Actores

### Usuario profesional

Corresponde al usuario autorizado que utiliza la aplicación para registrar información, ejecutar cálculos y consultar tratamientos.

### Administrador

Corresponde al usuario encargado de mantener y configurar la información utilizada por el sistema.

## Casos de uso

| Código | Caso de uso | Actor principal | Estado |
|---|---|---|---|
| CU01 | Iniciar sesión | Usuario profesional / Administrador | Implementado mediante acceso a AppSheet |
| CU02 | Registrar variables del tratamiento | Usuario profesional | Implementado |
| CU03 | Validar datos | Sistema | Implementado |
| CU04 | Ejecutar cálculos del tratamiento | Usuario profesional / Sistema | Implementado |
| CU05 | Calcular cantidad de producto comercial | Usuario profesional / Sistema | Implementado |
| CU06 | Calcular consumo estimado de agua | Sistema | Implementado |
| CU07 | Consultar resultados del tratamiento | Usuario profesional | Implementado |
| CU08 | Guardar tratamiento | Usuario profesional | Implementado |
| CU09 | Consultar historial | Usuario profesional | Implementado |
| CU10 | Exportar resultados | Usuario profesional | Funcionalidad futura |
| CU11 | Gestionar productos | Administrador | Configuración disponible desde AppSheet y fuente de datos |
| CU12 | Gestionar información asociada a productos | Administrador | Configuración disponible |
| CU13 | Gestionar usuarios desde la aplicación | Administrador | Funcionalidad futura |

## Flujo principal

El flujo general del sistema corresponde a:

```text
Inicio de sesión
      ↓
Registro de variables
      ↓
Validación de datos
      ↓
Ejecución de cálculos
      ↓
Visual


