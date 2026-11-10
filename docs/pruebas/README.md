# Pruebas del prototipo

La validación del prototipo se realizó mediante pruebas funcionales y pruebas de validación de entrada.

El objetivo fue verificar que los cálculos generados por la aplicación coincidieran con valores de referencia y que las reglas configuradas en AppSheet rechazaran datos fuera de los rangos establecidos.

## Pruebas funcionales

Se evaluaron diferentes escenarios de tratamiento utilizando productos, dosis, pesos y tamaños de lote distintos.

| Prueba | Producto | Concentración | Dosis mg/kg | Peso kg | Animales | Días | Resultado esperado |
|---|---|---:|---:|---:|---:|---:|---|
| PF01 | Amoxicilina | 50 % | 20 | 35 | 150 | 5 | 1,050 kg total |
| PF02 | Florfenicol | 10 % | 20 | 25 | 180 | 5 | 4,500 kg total |
| PF03 | Doxiciclina | 50 % | 15 | 60 | 160 | 5 | 1,440 kg total |
| PF04 | Fosfomicina | 10 % | 40 | 75 | 140 | 5 | 21,000 kg total |
| PF05 | Tilvalosina | 5 % | 4 | 145 | 85 | 5 | 4,930 kg total |
| PF06 | Tiamulina | 10 % | 12,5 | 230 | 55 | 5 | 7,906 kg total |

En los escenarios evaluados, los resultados generados por la aplicación coincidieron con los cálculos manuales de referencia.

## Fórmulas utilizadas

### Consumo estimado de agua por animal

```text
Consumo de agua = Peso promedio × 0,12
```

### Consumo total estimado del lote

```text
Consumo total = Consumo por animal × Número de animales
```

### Cantidad diaria de producto comercial

```text
Producto g/día =
(Dosis mg/kg × Peso kg × Número de animales)
/
(Concentración % × 10)
```

### Cantidad total de producto

```text
Producto total kg =
(Producto g/día × Días de tratamiento)
/
1000
```

## Pruebas de validación de entrada

También se verificó el comportamiento de las restricciones configuradas en el formulario.

| Código | Variable evaluada | Valor probado | Resultado esperado |
|---|---|---:|---|
| PV01 | Concentración | 0 | Rechazado |
| PV02 | Concentración | 50 | Aceptado |
| PV03 | Peso promedio | 0 | Rechazado |
| PV04 | Peso promedio | 150 | Aceptado |
| PV05 | Peso promedio | 300 | Rechazado |
| PV06 | Dosis | Mayor al doble de la dosis de referencia | Rechazado |
| PV07 | Dosis | Dentro del rango permitido | Aceptado |
| PV08 | Número de animales | 0 | Rechazado |
| PV09 | Número de animales | 100 | Aceptado |
| PV10 | Duración | 2 días | Rechazado |
| PV11 | Duración | 5 días | Aceptado |
| PV12 | Duración | 16 días | Rechazado |

Las pruebas confirmaron que las reglas configuradas en AppSheet aceptan los valores definidos como válidos y rechazan entradas fuera de los rangos establecidos.

## Reglas principales de validación

Entre las principales restricciones implementadas se encuentran:

```text
Concentración:
AND([_THIS] > 0, [_THIS] <= 100)
```

```text
Peso promedio:
AND([_THIS] > 0, [_THIS] < 300)
```

```text
Número de animales:
[_THIS] > 0
```

```text
Duración:
AND([_THIS] >= 3, [_THIS] <= 15)
```

La dosis utilizada también se encuentra limitada a un rango máximo definido con relación a la dosis de referencia.

## Resultado general

Las pruebas realizadas permitieron verificar:

- Correcto funcionamiento de las fórmulas.
- Coherencia entre cálculos manuales y resultados de la aplicación.
- Funcionamiento de las reglas de validación.
- Prevención de valores inválidos.
- Almacenamiento adecuado de los registros evaluados.

Estas evidencias complementan la validación funcional del prototipo dentro del alcance definido para la Fase 4.
