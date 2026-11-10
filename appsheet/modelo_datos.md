# Modelo de datos del prototipo

El prototipo utiliza Google Sheets como fuente inicial de almacenamiento y Google AppSheet como interfaz de captura, procesamiento y consulta.

La estructura principal se organiza alrededor de los registros de tratamientos y la información asociada a los productos comerciales.

## Tabla principal: Calculadora

La tabla `Calculadora` almacena los tratamientos registrados desde AppSheet.

Entre los campos principales se encuentran:

| Campo | Descripción |
|---|---|
| ID | Identificador único del registro |
| Fecha | Fecha del tratamiento o cálculo |
| Producto | Producto comercial seleccionado |
| Concentración | Concentración del producto en porcentaje |
| Dosis de referencia | Dosis configurada como valor orientador |
| Dosis utilizada | Dosis ingresada para el cálculo en mg/kg |
| Peso promedio | Peso promedio de los animales en kg |
| Número de animales | Cantidad de animales incluidos en el tratamiento |
| Duración | Número de días del tratamiento |
| Consumo estimado por animal | Consumo calculado a partir del 12 % del peso vivo |
| Consumo total del lote | Consumo estimado total de agua del grupo |
| Producto por día | Cantidad diaria de producto comercial requerida |
| Producto total | Cantidad total necesaria para completar el tratamiento |

## Información de productos

La aplicación utiliza información asociada a los productos comerciales para facilitar el cálculo.

Entre los datos utilizados se encuentran:

- Nombre del producto.
- Principio activo.
- Concentración.
- Dosis de referencia.

Esta información puede actualizarse desde las tablas asociadas a la aplicación y la configuración administrativa de AppSheet.

## Tabla auxiliar: ResumenProductos

Para algunas visualizaciones se utiliza una tabla auxiliar denominada `ResumenProductos`.

Esta tabla permite consolidar información sobre la cantidad total de producto utilizada por medicamento.

Ejemplo de fórmula utilizada en Google Sheets:

```text
=SUMAR.SI(Calculadora!C:C;A2;Calculadora!M:M)
```

La fórmula suma la cantidad total registrada en la tabla `Calculadora` para cada producto comercial.

## Flujo de datos

```text
Usuario
   ↓
Formulario AppSheet
   ↓
Registro en Calculadora
   ↓
Cálculos automáticos
   ↓
Google Sheets
   ↓
Historial / Detalle / Resúmenes / Gráficos
```

## Principios del modelo

El modelo de datos fue diseñado considerando los siguientes criterios:

- Simplicidad.
- Trazabilidad.
- Facilidad de mantenimiento.
- Separación entre datos ingresados y datos calculados.
- Posibilidad de ampliación futura.

## Escalabilidad

Google Sheets resulta adecuado para la etapa de prototipado y validación académica.

En una implementación futura con mayor volumen de información, concurrencia o número de usuarios, la estructura podrá migrarse a una base de datos relacional como PostgreSQL, MySQL o SQL Server.

## Nota

La estructura descrita corresponde al prototipo desarrollado durante la Fase 4 y puede evolucionar en versiones posteriores del sistema.
