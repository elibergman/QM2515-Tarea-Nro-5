# QM2515-Tarea-Nro-5
Programas de la materia de Introducción a la Quimiometría. Tarea Nro. 5
# Programa #1: Transformación Lineal y Regresión Lineal

Incorpore `numpy` y `matplotlib.pyplot` para manejar arreglos y visualizar datos. Tengo un conjunto de datos `x_datos` y `y_datos` que siguen una relación exponencial. Para linealizar esta relación y aplicar regresión lineal, transformo `x_datos` tomando su logaritmo natural, dado que la ecuación propuesta es `x=e^(y−b)/a`, la cual al linealizar se convierte en `ln(x)=ay−ab`. Utilizo `numpy.polyfit` para hallar la pendiente `m` y el intercepto `c` de la relación lineal entre `Y = ln(x_datos)` y `X = y_datos`.

Con `m` y `c`, despejo los parámetros originales `a` y `b` de la ecuación exponencial. Predigo `y` para `x=2.6` utilizando la relación exponencial con los parámetros encontrados. Gráfico los datos transformados y la línea de regresión para visualizar el ajuste.

Con esto, aplico métodos de regresión lineal a un problema que originalmente requiere un modelo no lineal, permitiéndome predecir valores y estimar los parámetros `a` y `b` eficientemente.

# Programa #2: Capacidad Calorífica vs Temperatura

# Python

Para analizar la relación entre la temperatura y la capacidad calorífica, empleé Python con bibliotecas específicas: `numpy` para la manipulación de datos, `matplotlib.pyplot` para la visualización gráfica y `scipy.stats` para realizar una regresión lineal.

Primero, definí dos arrays usando `numpy`: `T` para las temperaturas y `c` para las capacidades caloríficas. Luego, utilicé la función `linregress` de `scipy.stats`, que me proporcionó la pendiente y el intercepto de la mejor línea de ajuste para estos datos, así como el coeficiente de correlación (`r_value`).

Con estos parámetros de regresión en mano, generé un conjunto de puntos de temperatura `T_linea` con `numpy.linspace` y calculé sus correspondientes valores de capacidad calorífica `c_linea` utilizando la ecuación de la línea recta.

Para la visualización, usé `matplotlib.pyplot`. Grafiqué los datos originales con `plt.scatter` y la línea de regresión con `plt.plot`, añadiendo títulos y leyendas para claridad. El gráfico resultante mostró tanto los datos experimentales como la línea de regresión ajustada.

Finalmente, presenté los resultados de la regresión. Imprimí la ecuación lineal obtenida y calculé el coeficiente de determinación (R²). En este caso, el valor alto de R² sugirió una fuerte correlación lineal entre la temperatura y la capacidad calorífica.

