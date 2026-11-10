# Manual de usuario del prototipo

Este documento presenta una guía básica para utilizar el prototipo desarrollado en Google AppSheet para el cálculo y registro de tratamientos antimicrobianos administrados mediante agua de bebida en producción porcina.

## 1. Acceso a la aplicación

El usuario debe ingresar a la aplicación mediante el enlace autorizado de Google AppSheet.

El acceso depende de la configuración definida para el prototipo y de los usuarios habilitados durante la fase de validación.

## 2. Pantalla principal

Desde la pantalla principal es posible acceder a las funciones principales del sistema, entre ellas:

- Registro de un nuevo tratamiento.
- Consulta del historial.
- Visualización de registros almacenados.
- Consulta del tablero de control y gráficos.

## 3. Registro de un nuevo tratamiento

Para realizar un cálculo, el usuario debe ingresar las variables requeridas por el formulario.

Entre ellas se encuentran:

- Producto comercial.
- Concentración del producto.
- Dosis utilizada en mg/kg.
- Peso promedio de los animales en kg.
- Número de animales.
- Duración del tratamiento en días.

## 4. Consumo estimado de agua

El usuario no debe ingresar manualmente el consumo de agua.

La aplicación calcula automáticamente el consumo estimado utilizando una relación equivalente al 12 % del peso vivo por animal y por día.

La fórmula utilizada es:

```text
Consumo estimado por animal = Peso promedio × 0,12
```

Posteriormente, el sistema calcula:

```text
Consumo total del lote =
Consumo estimado por animal × Número de animales
```

## 5. Validación de datos

Antes de guardar el tratamiento, la aplicación verifica que las variables se encuentren dentro de los rangos definidos.

Entre las principales validaciones se encuentran:

- Concentración mayor que 0 y menor o igual a 100 %.
- Peso promedio mayor que 0 y menor que 300 kg.
- Número de animales mayor que 0.
- Duración entre 3 y 15 días.
- Dosis dentro del rango permitido.

Si un valor no cumple las condiciones establecidas, la aplicación no permite continuar hasta que el dato sea corregido.

## 6. Resultados del cálculo

Una vez ingresados los datos válidos, la aplicación calcula automáticamente:

- Consumo estimado de agua por animal.
- Consumo total estimado del lote.
- Cantidad diaria de producto comercial.
- Cantidad total de producto necesaria para completar el tratamiento.

Los campos calculados no pueden ser modificados directamente por el usuario.

## 7. Guardar el tratamiento

Después de verificar los datos y resultados, el usuario puede guardar el registro.

La información queda almacenada en la tabla asociada al prototipo y puede ser consultada posteriormente.

## 8. Consulta del historial

La sección de historial permite visualizar los tratamientos almacenados anteriormente.

Cada registro puede seleccionarse para consultar su información detallada.

Esto facilita revisar:

- Producto utilizado.
- Dosis.
- Peso promedio.
- Número de animales.
- Duración.
- Consumo estimado de agua.
- Cantidades calculadas.

## 9. Tablero de control

La aplicación incluye visualizaciones que permiten consultar información resumida sobre los tratamientos registrados.

Entre las visualizaciones implementadas se encuentran:

- Número de tratamientos por producto.
- Cantidad total de producto por medicamento.
- Consumo estimado de agua por tratamiento.
- Número de animales tratados por fecha.

Estas visualizaciones se integran en un tablero de control.

## 10. Alcance de la herramienta

La aplicación funciona como una herramienta de apoyo para realizar cálculos y registrar información.

El sistema:

- No realiza diagnósticos.
- No selecciona automáticamente el antimicrobiano.
- No prescribe tratamientos.
- No sustituye el criterio profesional del médico veterinario.

La definición del tratamiento y la dosis utilizada continúan siendo responsabilidad del profesional.

## 11. Limitaciones

El consumo de agua utilizado por el prototipo corresponde a una estimación basada en el 12 % del peso vivo diario.

Por lo tanto, los resultados deben interpretarse considerando que el consumo real puede variar según las condiciones productivas y ambientales.

La integración con mediciones reales de consumo de agua se considera una mejora futura.
