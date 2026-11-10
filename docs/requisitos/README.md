# Requisitos del sistema

Los requisitos del prototipo fueron definidos a partir del análisis del problema, los resultados del cuestionario aplicado a profesionales vinculados con producción porcina y las necesidades identificadas durante el desarrollo del proyecto.

## Requisitos funcionales implementados

### RF01 – Registro de datos del tratamiento
El sistema permite registrar las variables necesarias para realizar el cálculo.

### RF02 – Selección de producto
El usuario puede seleccionar el producto comercial utilizado en el tratamiento.

### RF03 – Registro de concentración
El sistema permite registrar o utilizar la concentración del producto seleccionado.

### RF04 – Registro de dosis
El usuario registra la dosis utilizada en mg/kg.

### RF05 – Estimación del consumo de agua
El sistema calcula automáticamente el consumo estimado de agua utilizando una relación equivalente al 12 % del peso vivo por animal y día.

### RF06 – Registro de duración
El sistema permite ingresar la duración del tratamiento.

### RF07 – Cálculo diario del producto
El sistema calcula automáticamente la cantidad diaria de producto comercial requerida.

### RF08 – Cálculo del consumo total de agua
El sistema determina el consumo estimado de agua correspondiente al grupo de animales.

### RF09 – Integración de variables
Los cálculos consideran la información registrada sobre peso promedio, número de animales, dosis, concentración y duración.

### RF10 – Cálculo total del tratamiento
El sistema calcula la cantidad total de producto necesaria para completar el tratamiento.

### RF11 – Validación de campos
El sistema verifica que los campos obligatorios contengan información válida.

### RF12 – Validación de valores
La aplicación genera restricciones ante valores nulos, negativos o fuera de los rangos definidos.

### RF13 – Almacenamiento de tratamientos
Los tratamientos realizados quedan almacenados en una fuente estructurada de datos.

### RF14 – Consulta de historial
El usuario puede consultar tratamientos registrados anteriormente.

### RF15 – Trazabilidad
Cada registro conserva información básica que permite identificar las condiciones utilizadas durante el cálculo.

### RF17 – Visualización de resultados
La aplicación muestra los resultados calculados y permite consultar posteriormente el detalle de cada tratamiento.

### RF18 – Identificación de campos y unidades
Los formularios presentan nombres de variables y unidades que permiten interpretar la información registrada.

### RF19 – Gestión de información técnica
La información utilizada por el prototipo puede actualizarse desde la configuración de AppSheet y las tablas asociadas.

## Requisitos funcionales pendientes o futuros

### RF16 – Exportación de resultados
La generación automatizada de reportes o archivos exportables se mantiene como una funcionalidad futura.

### RF20 – Advertencia profesional
El alcance del sistema se encuentra documentado como herramienta de apoyo y no como sistema de prescripción. Se plantea fortalecer en futuras versiones una advertencia permanente dentro de la interfaz.

### Gestión avanzada de usuarios
La administración completa de usuarios y roles desde la propia aplicación se considera una mejora futura.

## Requisitos no funcionales

### RNF01 – Usabilidad
La interfaz debe ser clara y comprensible para usuarios con diferentes niveles de experiencia.

### RNF02 – Confiabilidad
Los resultados deben coincidir con cálculos manuales de referencia previamente verificados.

### RNF03 – Integridad de datos
El sistema debe impedir el almacenamiento de registros con datos críticos inválidos.

### RNF04 – Accesibilidad
El prototipo puede utilizarse desde dispositivos compatibles con Google AppSheet.

### RNF05 – Mantenibilidad
Las reglas, expresiones y tablas deben poder modificarse sin reconstruir completamente la aplicación.

### RNF06 – Trazabilidad
Los registros deben conservar la información necesaria para identificar las condiciones utilizadas durante cada cálculo.

### RNF07 – Escalabilidad
La estructura debe permitir incorporar nuevas variables, reglas o fuentes de datos en versiones posteriores.

### RNF08 – Seguridad
El acceso a la aplicación y a los datos depende de la configuración de usuarios autorizados disponible en AppSheet.

### RNF09 – Consistencia
Los mismos datos de entrada deben generar resultados reproducibles.

### RNF10 – Adecuación funcional
Las funcionalidades implementadas deben corresponder con los objetivos y alcance definidos para el proyecto.

## Estado general

Los requisitos centrales relacionados con cálculo, validación, almacenamiento, historial y visualización fueron implementados y evaluados durante la Fase 4.

Las funciones de exportación avanzada, gestión interna de usuarios y ampliación del control administrativo se mantienen como oportunidades de desarrollo futuro.
