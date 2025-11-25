# Manipulación de Imágenes con Operaciones Matriciales en Excel

## Objetivo

El objetivo de esta tarea es **documentar** de manera clara y detallada el proceso de programación y las fórmulas utilizadas para realizar **operaciones matriciales** en Microsoft Excel, aplicadas a la **manipulación de imágenes**.

---

## Recursos y Herramientas

### Repositorio de Referencia

- **Guía de Markdown:** [https://github.com/JorgeTSW/DOCUMENTACION-MARKDOWN.git](https://github.com/JorgeTSW/DOCUMENTACION-MARKDOWN.git)
- **Importante:** Revisen la estructura de encabezados, el uso de listas, código y otros elementos de formato Markdown presentes en ese archivo.

---

## Documentos a Documentar

El archivo de documentación debe cubrir y explicar el contenido de **14 hojas de cálculo** en total, organizadas de la siguiente manera. La explicación debe detallar las fórmulas o el proceso de vinculación entre las hojas:

### 10 Hojas Base:

#### 5 Hojas de Imágenes Originales
- Contienen las imágenes originales representadas como **matrices de 30x30**.

#### 5 Hojas de Matrices Traspuestas
- Muestran las **matrices traspuestas** (Aᵀ) de las 5 imágenes originales.

### 4 Hojas de Operación:

1. **Multiplicación Escalar**
   - 1 hoja dedicada a la multiplicación escalar de una matriz (Imagen × Escalar).

2. **Suma de Dos Matrices**
   - 1 hoja dedicada a la suma de dos matrices (Imagen A + Imagen B).

3. **Resta de Dos Matrices**
   - 1 hoja dedicada a la resta de dos matrices (Imagen A - Imagen B).

4. **Composición de Matrices**
   - 1 hoja dedicada a la composición de matrices, específicamente la suma de dos multiplicaciones escalares: **c1A + c2B**.

---

## Documentación de las Imágenes en Hojas de Cálculo

Para este proyecto usé números en cada celda para representar colores. Básicamente pinté pixel por pixel usando valores numéricos y luego apliqué formato condicional para que se vean los colores.

### Imagen 1: Emoji Feliz 😊

La primera imagen es un emoji sonriente clásico. Está ubicado en las filas 2 a 17, ocupando un cuadro de más o menos 14x14 celdas.

**Sistema de colores que usé:**
- `0` = Negro (para los ojos y la boca)
- `1` = Amarillo (para la cara)

Para pintar esto en la hoja de cálculo, primero llené todas las celdas con 0s y 1s según donde quería cada color. Luego usé formato condicional para que automáticamente se pintaran:
```
Si la celda = 0 → pintar de negro
Si la celda = 1 → pintar de amarillo
```

Los ojos los hice con rectángulos negros alrededor de las filas 7-8, y la sonrisa es una curva que va de la fila 11 a la 13. Todo el contorno de la cara es amarillo para que se vea redondo.

**Matriz del Emoji:**
```
  A B C D E F G H I J K L M N
2 . . . 1 1 1 1 1 1 1 1 . . .
3 . . 1 1 1 1 1 1 1 1 1 1 . .
4 . 1 1 1 1 1 1 1 1 1 1 1 1 .
5 1 1 1 1 1 1 1 1 1 1 1 1 1 1
6 1 1 1 1 1 1 1 1 1 1 1 1 1 1
7 1 1 1 0 0 0 1 1 0 0 0 1 1 1
8 1 1 1 0 0 0 1 1 0 0 0 1 1 1
9 1 1 1 1 1 1 1 1 1 1 1 1 1 1
10 1 1 1 1 1 1 1 1 1 1 1 1 1 1
11 1 1 0 0 1 1 1 1 1 1 0 0 1 1
12 1 1 1 0 0 0 0 0 0 0 0 1 1 1
13 . 1 1 1 0 0 0 0 0 0 1 1 1 .
14 . 1 1 1 1 1 1 1 1 1 1 1 1 .
15 . . 1 1 1 1 1 1 1 1 1 1 . .
16 . . . 1 1 1 1 1 1 1 1 . . .
17 . . . . . . . . . . . . . .
```

Donde:
- `1` = Amarillo (cara)
- `0` = Negro (ojos y boca)
- `.` = Vacío/transparente

---

### Imagen 2: Amon us

Esta es un among us, como las que ves en videojuegos retro. La coloqué más abajo, empezando en la fila 32.

**Sistema de colores:**
- `0` = Blanco (para el fondo y huecos internos)
- `1` = Azul (el relleno de la letra)
- `2` = Negro (el contorno)


La parte más difícil fue la pata diagonal de la R y hacer que el círculo superior se viera bien en pixel art.

**Matriz de among us**
```
    D E F G H I J K L M N
32  . . . 2 2 2 2 2 2 . .
33  . . 2 2 1 1 1 2 2 2 .
34  . 2 2 1 1 1 1 1 1 2 2
35  2 2 1 1 1 1 1 1 1 1 2
36  2 2 0 0 0 1 1 1 2 2 2
37  2 2 1 1 1 1 1 1 1 1 2
38  2 2 0 0 0 1 1 2 2 2 .
39  2 2 1 1 1 1 1 1 1 2 .
40  2 2 1 1 1 1 1 1 1 1 2
41  2 2 1 1 1 1 1 1 1 2 2
42  2 2 1 1 1 1 1 1 2 2 .
43  . 2 2 1 1 1 1 2 2 . .
44  . . 2 2 1 1 2 2 . . .
45  . . . 2 2 2 2 . . . .
46  . . . 2 2 1 1 2 . . .
47  . . . . 2 2 1 1 2 . .
48  . . . . . 2 2 2 2 . .
49  . . . . . . 2 2 . . .
50  . . . . . . . . . . .
```

Donde:
- `2` = Negro (contorno)
- `1` = Azul (relleno)
- `0` = Blanco (huecos internos)
- `.` = Vacío/transparente

---

### Imagen 3: Calavera

Aquí hice una calavera. Es blanco y negro nada más, muy simple.

**Sistema de colores:**
- `0` = Blanco (fondo)
- `1` = Negro (líneas y detalles)

La calavera tiene su cabeza rectangular, dos ojos cuadrados, una nariz pequeñita en el centro y una boca con dientes. Todo el contorno es de 1 píxel de grosor. Esta imagen me sirvió de base para hacer varias operaciones matriciales después.

**Matriz de la Calavera :**
```
    E F G H I J K L M N O
54  . . . . . . . . . . .
55  . . . 1 1 1 1 1 1 . .
56  . . 1 1 0 0 0 0 1 1 .
57  . 1 1 0 0 0 0 0 0 1 1
58  1 1 0 0 0 0 0 0 0 0 1
59  1 1 0 0 0 0 0 0 0 0 1
60  1 1 0 0 0 0 0 0 0 0 1
61  1 1 0 0 1 1 0 0 1 1 1
62  1 1 0 0 1 1 0 0 1 1 1
63  1 1 0 0 0 0 0 0 0 0 1
64  1 1 0 0 0 1 1 0 0 0 1
65  1 1 0 0 0 0 0 0 0 0 1
66  1 1 0 0 1 0 1 0 1 0 1
67  . 1 1 0 1 0 1 0 1 1 .
68  . . 1 1 1 0 1 1 1 . .
69  . . . 1 1 0 1 1 . . .
70  . . . . 1 1 1 . . . .
71  . . . . . . . . . . .
```

Donde:
- `1` = Negro (contorno y detalles)
- `0` = Blanco (relleno interno)
- `.` = Vacío/transparente

---

### Imagen 4 y 5: Más Calaveras

Las siguientes calaveras son copias o transformaciones de la tercera. Una es exactamente igual (la usé para hacer operaciones como restas de matrices), y la otra está rotada o volteada, que es el resultado de hacer la trasposición matricial.

Para mover las imágenes de lugar sin tener que copiar y pegar todo manualmente, usé fórmulas. Por ejemplo, si quería la misma imagen pero 10 filas más abajo, en cada celda nueva ponía una fórmula que apuntara a la celda original pero 10 filas arriba.

**Imagen 4: Calavera Duplicada (filas 78-95)**

Esta es idéntica a la Imagen 3. La usé principalmente para hacer operaciones de resta (Imagen 3 - Imagen 4 = 0), lo cual demuestra que ambas matrices son iguales.
```
Misma matriz que la Imagen 3
```

**Imagen 5: Calavera Traspuesta (filas 99-120)**

Esta es la versión traspuesta de la calavera original. Lo que antes eran filas ahora son columnas y viceversa. Es como si rotaras la imagen 90 grados y la voltearas.
```
    C D E F G H I J K L M N O P Q R S T U V W
99  . . . . . . . . . . . . . . . . . . . . .
100 . 1 1 1 1 1 1 1 1 1 1 1 1 . . . . . . . .
101 . 1 0 0 0 0 0 0 0 0 0 0 1 1 . . . . . . .
102 . . 1 0 0 0 0 0 0 0 0 0 0 1 1 . . . . . .
103 . . . 1 0 0 0 1 1 0 0 0 1 0 1 1 . . . . .
104 . . . . 0 0 0 1 1 0 1 0 0 0 0 1 1 . . . .
105 . . . . 0 0 0 0 0 0 1 0 1 0 1 0 1 1 . . .
106 . . . . 0 0 0 0 0 0 1 0 1 0 1 1 1 . . . .
107 . . . . 0 0 0 1 1 0 0 0 1 0 1 1 . . . . .
108 . . . . 0 0 0 1 1 0 0 0 0 1 1 . . . . . .
109 . . . . 1 0 0 0 0 0 0 0 0 1 . . . . . . .
110 . . . 1 1 0 0 0 0 0 0 0 1 . . . . . . . .
111 . . 1 1 1 1 0 0 0 1 0 1 . . . . . . . . .
112 . 1 1 1 1 1 1 1 1 1 1 . . . . . . . . . .
113 . . . . . . . . . . . . . . . . . . . . .
```

Donde:
- `1` = Negro
- `0` = Blanco
- `.` = Vacío/transparente

Nota: Esta matriz es más ancha porque las filas se convirtieron en columnas.

---

## Operaciones Matriciales

### 1. Trasposición de Matrices

La trasposición es voltear la matriz, cambiando filas por columnas. Si tengo una imagen en horizontal, la trasposición la pone en vertical.

**Cómo lo hice:**
Si mi imagen original está en las celdas A1:Z30, para hacer la traspuesta en otra parte de la hoja, digamos empezando en A35, uso esta fórmula en la celda A35:
```
=INDIRECTO(DIRECCION(COLUMNA(A35)-COLUMNA($A$35)+FILA($A$1), FILA(A35)-FILA($A$35)+COLUMNA($A$1)))
```

O si tu hoja de cálculo tiene la función TRANSPONER:
```
=TRANSPONER(A1:Z30)
```

Lo que hace es que la fila 1 de la original se vuelve la columna 1 de la traspuesta, la fila 2 se vuelve columna 2, y así. Es como rotar la imagen 90 grados.

---

### 2. Multiplicación Escalar

Esta operación multiplica cada pixel de la imagen por un número. Es útil para hacer la imagen más clara o más oscura.

**Ejemplo:**
Si tengo mi calavera en A1:Z30 y quiero multiplicarla por 2, en mi hoja de operación pongo:
```
=A1*2
```

Y arrastro esa fórmula por todo el rango. Si en la celda A1 había un 1, ahora habrá un 2. Si había un 0, sigue siendo 0.

**Uso práctico:**
Digamos que pongo el escalar en una celda fija, por ejemplo la celda AA1 tiene el valor 3. Entonces mi fórmula sería:
```
=A1*$AA$1
```

Los signos de dólar hacen que siempre se multiplique por esa misma celda AA1, sin importar dónde copies la fórmula.

---

### 3. Suma de Matrices

Aquí sumo dos imágenes pixel por pixel. Si tengo el emoji en una hoja y la calavera en otra, puedo sumarlas.

**Ejemplo:**
Supongamos que:
- Imagen A (emoji) está en la hoja "Emoji" en las celdas A1:Z30
- Imagen B (calavera) está en la hoja "Calavera" en las celdas A1:Z30

En mi hoja de "Suma", en la celda A1 pongo:
```
=Emoji!A1+Calavera!A1
```

Y arrastro por todo el rango. Lo que hace es sumar los valores numéricos de cada pixel. Si en ambas imágenes hay un 1 en esa posición, el resultado será 2.

**¿Para qué sirve?**
Puedes combinar dos imágenes. Por ejemplo, si sumas la calavera con la R, aparecen ambas en la misma imagen (aunque se ven raras porque los valores se suman).

---

### 4. Resta de Matrices

Es lo mismo que la suma pero restando. Útil para ver diferencias entre dos imágenes.

**Ejemplo:**
Si resto la calavera menos ella misma:
```
=Calavera!A1-Calavera2!A1
```

El resultado es todo ceros, porque cada pixel se resta con su copia exacta.

Pero si resto dos imágenes diferentes, digamos emoji menos calavera:
```
=Emoji!A1-Calavera!A1
```

Los pixeles que eran iguales quedan en 0, y los diferentes muestran la diferencia. Pueden salir números negativos si la segunda imagen tiene valores mayores.

---

### 5. Composición de Matrices (Combinación Lineal)

Esta es la operación más compleja. Combino dos imágenes pero cada una multiplicada por su propio escalar primero.

**Fórmula general:** c1×A + c2×B

Donde:
- A y B son dos imágenes diferentes
- c1 y c2 son escalares (números que yo decido)

**Ejemplo práctico:**
Digamos que quiero combinar 3 veces el emoji más 2 veces la calavera. 
- Escalar 1 (c1) = 3, está en la celda AA1
- Escalar 2 (c2) = 2, está en la celda AA2
- Emoji está en la hoja "Emoji", celdas A1:Z30
- Calavera está en la hoja "Calavera", celdas A1:Z30

En mi hoja de "Composición", celda A1:
```
=($AA$1*Emoji!A1)+($AA$2*Calavera!A1)
```

Esto multiplica cada pixel del emoji por 3, cada pixel de la calavera por 2, y luego los suma. El resultado es una mezcla de ambas imágenes donde el emoji "pesa" más porque su escalar es mayor.

---

## Formato Condicional

Para que los números se vean como colores, usé el formato condicional. Aquí te explico cómo:

### Para el Emoji (0=negro, 1=amarillo):

1. Selecciono todo el rango de celdas donde está el emoji
2. Voy a Formato → Formato condicional
3. Agrego regla: Si el valor de la celda es igual a 0, formato de relleno negro
4. Agrego otra regla: Si el valor es igual a 1, formato de relleno amarillo

### Para la R (0=blanco, 1=azul, 2=negro):

1. Selecciono el rango
2. Primera regla: valor = 0 → fondo blanco
3. Segunda regla: valor = 1 → fondo azul
4. Tercera regla: valor = 2 → fondo negro

### Para las calaveras (0=blanco, 1=negro):

1. Selecciono el rango
2. Primera regla: valor = 0 → fondo blanco
3. Segunda regla: valor = 1 → fondo negro

También puedes ocultar los números poniendo el color de fuente igual al color de fondo, así solo ves los colores y no los números.

---

## Ejemplos de Fórmulas Completas

### Traslación (mover imagen 10 celdas a la derecha):

Si mi imagen original está en A1:A30, para moverla 10 columnas a la derecha, en la celda K1 pongo:
```
=A1
```

Y cuando arrastro hacia la derecha y abajo, automáticamente K1 toma A1, K2 toma A2, etc.

O puedes hacerlo dinámico:
```
=INDIRECTO(DIRECCION(FILA(), COLUMNA()-10))
```

Esto siempre toma la celda que está 10 columnas a la izquierda.

### Escalar toda una imagen por 0.5:

En la celda AA1 pongo: 0.5

En mi hoja de resultado, celda A1:
```
=ImagenOriginal!A1*$AA$1
```

Arrastro por todo el rango y cada pixel se multiplica por 0.5

### Restar dos imágenes idénticas para verificar que son iguales:
```
=Calavera1!A1-Calavera2!A1
```

Si el resultado es puro ceros, las imágenes son idénticas.

---

## Instrucciones Detalladas

### Parte 1: Crear un Branch para la Documentación

1. Asegúrate de estar en tu repositorio:
```bash
   cd ruta/a/tu/repositorio
```

2. Asegúrate de tener los últimos cambios del main:
```bash
   git checkout main
   git pull origin main
```

3. Crear un nuevo branch llamado "documentacion3":
```bash
   git checkout -b documentacion3
```

### Parte 2: Estructura del Documento

Tu documentación debe incluir:

- **Título y descripción** del proyecto
- **Explicación de cada hoja** de cálculo
- **Fórmulas utilizadas** con ejemplos
- **Capturas de pantalla** (opcional pero recomendado)
- **Proceso de vinculación** entre hojas

### Parte 3: Subir la Documentación

1. Agregar los archivos modificados:
```bash
   git add README.md
```

2. Hacer commit con mensaje descriptivo:
```bash
   git commit -m "Documentación de operaciones matriciales en hojas de cálculo"
```

3. Subir el branch al repositorio remoto:
```bash
   git push origin documentacion3
```

4. Crear un **Pull Request** en GitHub desde el branch `documentacion3` hacia `main`.

---

## Consejos

- Documenta **cada fórmula** que uses
- Explica **por qué** elegiste esa fórmula
- Incluye **ejemplos numéricos** cuando sea posible
- Usa **capturas de pantalla** para claridad visual
- Mantén la documentación **organizada y clara**

---

## Autor

Enrique Zavala Martinez

## Fecha

Noviembre 2025
