# Sistema de apoyo a la decisión para tratamientos antimicrobianos en porcicultura

Proyecto académico desarrollado en el marco del curso **Proyecto de Grado** del programa de Ingeniería de Sistemas de la Universidad Nacional Abierta y a Distancia - UNAD.

El proyecto consiste en el desarrollo de un prototipo funcional orientado al cálculo, registro y consulta de tratamientos antimicrobianos administrados mediante agua de bebida en producción porcina.

## Objetivo

Desarrollar un sistema de apoyo a la decisión que permita estandarizar el cálculo de tratamientos antimicrobianos administrados por agua de bebida, reducir errores de conversión, mejorar la trazabilidad de los registros y facilitar la consulta de información histórica.

## Tecnologías utilizadas

- Google AppSheet
- Google Sheets
- Google Forms
- GitHub
- Microsoft Word
- Herramientas de análisis y documentación académica

## Funcionalidades implementadas

El prototipo permite:

- Registrar variables asociadas al tratamiento.
- Seleccionar el producto comercial.
- Registrar la dosis utilizada por el profesional.
- Registrar el peso promedio de los animales.
- Registrar el número de animales.
- Registrar la duración del tratamiento.
- Calcular automáticamente el consumo estimado de agua.
- Calcular el consumo total estimado de agua del lote.
- Calcular la cantidad diaria de producto comercial requerida.
- Calcular la cantidad total de producto necesaria para completar el tratamiento.
- Aplicar reglas de validación sobre los datos ingresados.
- Almacenar los tratamientos realizados.
- Consultar el historial de tratamientos.
- Visualizar el detalle de cada registro.
- Consultar gráficos y un tablero de control.

## Cálculo del consumo de agua

Para el prototipo se utiliza una estimación equivalente al **12 % del peso vivo por animal y por día**.

La fórmula utilizada es:

**Consumo estimado de agua por animal = Peso promedio × 0,12**

Posteriormente:

**Consumo total estimado del lote = Consumo por animal × Número de animales**

Este valor corresponde a una estimación y no sustituye una medición directa del consumo de agua en condiciones reales de producción.

## Alcance del sistema

La aplicación funciona como una herramienta de apoyo al cálculo y al registro de información.

El sistema no realiza diagnóstico, no selecciona automáticamente el antimicrobiano y no sustituye la prescripción ni el criterio profesional del médico veterinario.

La definición del tratamiento, selección del producto y establecimiento de la dosis continúan siendo responsabilidad del profesional.

## Validación del prototipo

El sistema fue evaluado mediante:

- Pruebas funcionales con escenarios controlados.
- Comparación entre resultados manuales y resultados generados por la aplicación.
- Pruebas de validación de datos de entrada.
- Evaluación preliminar de usabilidad con cinco participantes.

La prueba de usabilidad obtuvo un promedio general de **4,6 sobre 5**.

## Nivel de madurez tecnológica

De acuerdo con las funcionalidades implementadas y las pruebas realizadas, el prototipo presenta características compatibles con un **TRL 5**, debido a que sus principales componentes fueron integrados y evaluados mediante escenarios representativos del proceso de cálculo.

## Limitaciones

Entre las principales limitaciones actuales se encuentran:

- El consumo de agua se estima y no se obtiene directamente desde medidores instalados en granja.
- La validación se realizó principalmente mediante escenarios controlados.
- Se requiere ampliar la evaluación con un mayor número de usuarios.
- Se requiere validación futura en condiciones productivas reales.
- La exportación automatizada de resultados y la gestión avanzada de usuarios se consideran funcionalidades futuras.

## Estructura del repositorio

```text
docs/
├── arquitectura/
├── capturas/
├── casos-de-uso/
├── kanban/
├── manual-usuario/
├── pruebas/
├── requisitos/
├── trl5/
└── usabilidad/

appsheet/
data/
```

La carpeta `docs` contiene la documentación técnica y las evidencias del proyecto.

La carpeta `appsheet` contiene información relacionada con expresiones, validaciones y estructura lógica del prototipo.

La carpeta `data` contiene datos ficticios o anonimizados utilizados exclusivamente para fines académicos y de validación.

## Equipo de trabajo

- Ricardo Andrés Henao Agudelo
- Jefri Alexander Martinez Alvarez
- David Fernando Monroy Gutierrez

## Tutor

Daniel Andrés Guzmán Arevalo

## Institución

Universidad Nacional Abierta y a Distancia - UNAD  
Escuela de Ciencias Básicas, Tecnología e Ingeniería - ECBTI  
Programa de Ingeniería de Sistemas

## Estado del proyecto

Prototipo funcional desarrollado y validado mediante pruebas controladas durante la Fase 4 del proyecto de grado.

## Nota

Este repositorio tiene fines exclusivamente académicos. No contiene información clínica real, datos personales sensibles ni información productiva confidencial de granjas.
