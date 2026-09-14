# Semana 05 · Visualización con Matplotlib y Seaborn (IRIS)

**Alumno:** José Pablo Herrera Fernández
**Materia:** Programación para la Inteligencia Artificial · MAPS
**Profesora:** M. en C. Gabriela Martínez

## Qué hay en esta carpeta

| Archivo | Qué es |
| --- | --- |
| `Semana_05_IRIS_Matplotlib_Seaborn_ORIGINAL.ipynb` | El notebook tal como lo entregó la profesora, **sin una sola modificación**. Sirve de referencia para comparar. |
| `Semana_05_IRIS_Matplotlib_Seaborn_RESUELTO.ipynb` | El mismo notebook con mis soluciones **agregadas**. Ninguna celda original fue borrada ni editada. |

## Cómo está resuelto

El notebook original trae 13 celdas con `TODO` (los retos 2 al 13 más el reto integrador) y las
celdas de interpretación en blanco. En la versión resuelta, cada bloque queda así:

```
[celda original con los TODO]        ← intacta, tal cual venía
[markdown: "✅ Reto N · copia corregida" + qué hice y por qué]   ← agregada
[celda de código con mi solución comentada]                      ← agregada
[celda original "Interpretación del reto"]                       ← intacta
[markdown: "Mi respuesta: ..."]                                  ← agregada
```

Así se ve de un vistazo la diferencia entre el punto de partida y lo que hice, sin perder el
enunciado.

Se agregaron 40 celdas nuevas (de 71 a 111). Ninguna celda original cambió: se puede comprobar con

```bash
git diff --no-index --stat \
  Semana_05_IRIS_Matplotlib_Seaborn_ORIGINAL.ipynb \
  Semana_05_IRIS_Matplotlib_Seaborn_RESUELTO.ipynb
```

## Verificación

El notebook resuelto se ejecutó de principio a fin con el kernel reiniciado (pandas 3.0.5,
matplotlib 3.11.2, seaborn 0.13.2): **0 celdas con error**. Se generan las cinco figuras
esperadas en `salidas_semana05/`:

- `matplotlib_medias_petalo.png` (ejemplo de la sección 7)
- `seaborn_pairplot_iris.png` (ejemplo de la sección 12)
- `reto7_virginica.png` (reto 7)
- `reto_final_matplotlib.png` y `reto_final_seaborn.png` (reto integrador)

Cada guardado se verifica con `.exists()` dentro del propio notebook.

## Reto integrador

**Pregunta elegida:** ¿el ancho del sépalo permite distinguir a setosa de las otras dos especies
tan bien como lo hace el pétalo?

**Respuesta corta:** no. Setosa tiene el sépalo más ancho en promedio (3.43 cm contra 2.77 y
2.97 cm), pero 96 de las 100 flores no-setosa caen dentro del rango de ancho de sépalo de setosa
(2.3–4.4 cm). En el pétalo, en cambio, hay un hueco vacío entre 1.9 y 3.0 cm: cero traslape.

## Cómo abrirlo en Colab

Descargar `Semana_05_IRIS_Matplotlib_Seaborn_RESUELTO.ipynb` y subirlo con
*Archivo → Subir cuaderno*. El dataset IRIS completo va incrustado en el propio notebook, así que
no hace falta conexión ni montar Drive.
