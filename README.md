# Respuestas Determinantes

## Ejercicio 1: Determinantes 2×2

**Matriz A:**
```
| 5  2 |
| 3  1 |
```
- det(A) = 5×1 - 2×3 = 5 - 6 = **-1**

**Matriz B:**
```
| -1   4 |
|  2  -8 |
```
- det(B) = -1×(-8) - 4×2 = 8 - 8 = **0**

**Matriz C:**
```
| 6  9 |
| 2  3 |
```
- det(C) = 6×3 - 9×2 = 18 - 18 = **0**

**Matriz D:**
```
|  0  5 |
| -5  0 |
```
- det(D) = 0×0 - 5×(-5) = 0 + 25 = **25**

---

## Ejercicio 2: Regla de Sarrus

**Matriz E:**
```
| 1  2  3 |
| 0  1  4 |
| 5  6  0 |
```
det(E) = (1×1×0) + (2×4×5) + (3×0×6) - (3×1×5) - (1×4×6) - (2×0×0)
- det(E) = 0 + 40 + 0 - 15 - 24 - 0 = **1**

**Matriz F:**
```
| 2  -1   3 |
| 1   4   0 |
| 3   2  -2 |
```
det(F) = (2×4×(-2)) + (-1×0×3) + (3×1×2) - (3×4×3) - (2×0×2) - (-1×1×(-2))
- det(F) = -16 + 0 + 6 - 36 - 0 - 2 = **-48**

---

## Ejercicio 3: Método de Cofactores

**Matriz G:**
```
|  1  0  2 |
| -1  3  1 |
|  2  0  1 |
```
Expandiendo por columna 2 (tiene ceros):
```
det(G) = 3 × | 1  2 |
             | 2  1 |
```
- det(G) = 3 × (1 - 4) = 3 × (-3) = **-9**

---

## Ejercicio 4: Verificar Propiedades

**Matriz A:**
```
| 2  1 |
| 1  3 |
```

**Matriz B:**
```
| 1  2 |
| 3  1 |
```

### Propiedad 1: det(AB) = det(A) × det(B)

- det(A) = 2×3 - 1×1 = 6 - 1 = **5**
- det(B) = 1×1 - 2×3 = 1 - 6 = **-5**
- det(A) × det(B) = 5 × (-5) = **-25**

**Producto AB:**
```
|  5  5 |
| 10  5 |
```
- det(AB) = 5×5 - 5×10 = 25 - 50 = **-25** ✓

### Propiedad 2: det(Aᵀ) = det(A)

**Matriz Aᵀ:**
```
| 2  1 |
| 1  3 |
```
- det(Aᵀ) = 2×3 - 1×1 = **5** = det(A) ✓

---

## Ejercicio 5: Aplicación Geométrica

**Vectores:** u = (3, 2) y v = (1, 4)

### a) Área del paralelogramo
```
| 3  1 |
| 2  4 |
```
- Área = |det| = |3×4 - 1×2| = |12 - 2| = **10 unidades²**

### b) Si intercambias los vectores
```
| 1  3 |
| 4  2 |
```
- det(v, u) = 1×2 - 3×4 = 2 - 12 = **-10**
- |det| = |-10| = **10 unidades²** (misma área, signo opuesto)

### c) ¿Qué significa el signo?
- **(+)** = vectores giran en sentido contrahorario
- **(-)** = vectores giran en sentido horario
- El signo indica la **orientación** del paralelogramo en el plano
