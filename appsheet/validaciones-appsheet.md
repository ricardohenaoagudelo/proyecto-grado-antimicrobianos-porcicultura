# Validaciones implementadas en AppSheet

Este documento resume las principales reglas de validación configuradas en el prototipo para reducir errores de digitación y evitar el almacenamiento de valores fuera de los rangos definidos.

## 1. Concentración del producto

La concentración debe ser mayor que 0 y menor o igual a 100.

```text
AND([_THIS] > 0, [_THIS] <= 100)
```

### Comportamiento esperado

- 0 % → rechazado
- 50 % → aceptado
- Valores mayores a 100 % → rechazados

---

## 2. Peso promedio de los animales

El peso promedio debe ser mayor que 0 kg y menor que 300 kg.

```text
AND([_THIS] > 0, [_THIS] < 300)
```

### Comportamiento esperado

- 0 kg → rechazado
- 150 kg → aceptado
- 300 kg → rechazado

---

## 3. Número de animales

El número de animales debe ser mayor que cero.

```text
[_THIS] > 0
```

### Comportamiento esperado

- 0 animales → rechazado
- 100 animales → aceptado

---

## 4. Duración del tratamiento

La duración permitida se encuentra entre 3 y 15 días.

```text
AND([_THIS] >= 3, [_THIS] <= 15)
```

### Comportamiento esperado

- 2 días → rechazado
- 5 días → aceptado
- 16 días → rechazado

---

## 5. Dosis utilizada

La dosis debe ser mayor que cero y no superar el doble de la dosis de referencia configurada.

```text
AND(
  [_THIS] > 0,
  [_THIS] <= ([Dosis sugerida] * 2)
)
```

> El nombre exacto del campo de referencia puede variar según la configuración de la tabla utilizada en AppSheet.

### Comportamiento esperado

- Valores iguales o menores al límite definido → aceptados.
- Valores superiores al doble de la dosis de referencia → rechazados.

---

## 6. Campos obligatorios

Las variables críticas del tratamiento fueron configuradas como obligatorias para evitar registros incompletos.

Entre ellas se encuentran:

- Producto comercial.
- Concentración.
- Dosis.
- Peso promedio.
- Número de animales.
- Duración del tratamiento.

---

## 7. Protección de campos calculados

Los campos gener
