# Expresiones principales de AppSheet

Este documento resume las principales expresiones y fórmulas utilizadas en el prototipo para calcular tratamientos antimicrobianos administrados mediante agua de bebida en producción porcina.

## 1. Consumo estimado de agua por animal

Para el prototipo se utiliza una estimación equivalente al **12 % del peso vivo por animal y por día**.

### Fórmula

```text
Consumo de agua por animal (L/día) =
Peso promedio (kg) × 0,12
```

### Ejemplo

Para un animal de 35 kg:

```text
35 × 0,12 = 4,2 L/día
```

Por lo tanto, el consumo estimado es:

```text
4,2 litros por animal por día
```

---

## 2. Consumo total estimado de agua del lote

El consumo total se obtiene multiplicando el consumo estimado por animal por el número de animales.

### Fórmula

```text
Consumo total del lote (L/día) =
Consumo por animal × Número de animales
```

### Ejemplo

Para 150 animales de 35 kg:

```text
4,2 × 150 = 630 L/día
```

El consumo estimado total del lote corresponde a:

```text
630 litros por día
```

---

## 3. Cantidad diaria de producto comercial

La cantidad diaria de producto se calcula utilizando:

- Dosis en mg/kg.
- Peso promedio en kg.
- Número de animales.
- Concentración del producto en porcentaje.

### Fórmula

```text
Producto (g/día) =
(Dosis mg/kg × Peso kg × Número de animales)
/
(Concentración % × 10)
```

El factor `10` permite convertir la concentración porcentual del producto a miligramos de principio activo por gramo de producto.

### Ejemplo

Amoxicilina al 50 %:

```text
Dosis = 20 mg/kg
Peso = 35 kg
Animales = 150
Concentración = 50 %
```

Cálculo:

```text
(20 × 35 × 150) / (50 × 10)
= 210 g/día
```

---

## 4. Cantidad total de producto para el tratamiento

La cantidad total requerida se obtiene multiplicando la cantidad diaria por la duración del tratamiento.

### Fórmula

```text
Producto total (kg) =
Producto g/día × Días de tratamiento / 1000
```

### Ejemplo

Para una administración de 210 g/día durante 5 días:

```text
210 × 5 / 1000
= 1,05 kg
```

El tratamiento requiere:

```text
1,05 kg de producto comercial
```

---

## 5. Principios de funcionamiento

Las expresiones fueron configuradas para que los resultados calculados automáticamente no puedan ser modificados directamente por el usuario.

El usuario registra las variables necesarias para el tratamiento y la aplicación ejecuta los cálculos de manera automática.

Las principales variables de entrada son:

- Producto comercial.
- Concentración.
- Dosis utilizada.
- Peso promedio.
- Número de animales.
- Duración del tratamiento.

Las principales variables calculadas son:

- Consumo estimado de agua por animal.
- Consumo total del lote.
- Cantidad diaria de producto.
- Cantidad total de producto requerida.

## Nota técnica

Las expresiones documentadas corresponden al prototipo académico desarrollado durante la Fase 4.

El consumo de agua utilizado corresponde a una estimación y no a una medición directa realizada en granja.
