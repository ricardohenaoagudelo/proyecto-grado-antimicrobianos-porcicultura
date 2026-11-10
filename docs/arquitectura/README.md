# Arquitectura del sistema

El prototipo fue desarrollado utilizando **Google AppSheet** como plataforma principal de interacción y procesamiento, y **Google Sheets** como fuente inicial de almacenamiento de información.

La arquitectura se organiza en cuatro componentes principales:

## 1. Entrada de datos

Corresponde a los formularios utilizados por el usuario para registrar las variables necesarias para el cálculo del tratamiento, entre ellas:

- Producto comercial.
- Concentración del producto.
- Dosis utilizada.
- Peso promedio de los animales.
- Número de animales.
- Duración del tratamiento.

## 2. Procesamiento

La lógica del sistema se encuentra configurada mediante expresiones, fórmulas y reglas de validación dentro de AppSheet.

Esta capa permite:

- Validar los datos ingresados.
- Estimar el consumo de agua.
- Calcular el consumo total de agua del lote.
- Calcular la cantidad diaria de producto comercial.
- Calcular la cantidad total requerida para completar el tratamiento.

## 3. Almacenamiento

Google Sheets funciona como repositorio estructurado de los registros generados por la aplicación.

Los datos almacenados incluyen información relacionada con:

- Fecha del tratamiento.
- Producto utilizado.
- Dosis.
- Peso promedio.
- Número de animales.
- Duración del tratamiento.
- Consumo estimado de agua.
- Resultados calculados.

## 4. Consulta y visualización

La aplicación permite posteriormente consultar los tratamientos registrados mediante:

- Historial de tratamientos.
- Vista de detalle de cada registro.
- Gráficos.
- Tablero de control.

## Flujo general de información

```text
Usuario
   ↓
Formulario AppSheet
   ↓
Validaciones y reglas de cálculo
   ↓
Resultados del tratamiento
   ↓
Google Sheets
   ↓
Historial / Detalle / Gráficos / Dashboard
```

## Consideraciones de escalabilidad

La arquitectura utilizada corresponde a una solución apropiada para la etapa de prototipado y validación controlada.

En versiones posteriores, la estructura podrá evolucionar hacia fuentes de datos con mayor capacidad y concurrencia, como bases de datos relacionales, manteniendo la lógica general del sistema.
