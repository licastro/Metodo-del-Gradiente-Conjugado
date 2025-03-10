# Método de Gradiente Conjugado 🔄

Repositorio para la implementación del **método de gradiente conjugado** para la resolución de sistemas de ecuaciones lineales.

## 📌 Objetivo  
El objetivo de este trabajo es implementar el **método de gradiente conjugado** para resolver sistemas de ecuaciones lineales de la forma `Ax = b`, donde `A` es una matriz definida positiva.

## 📖 Descripción  

El **método de gradiente conjugado** es un algoritmo iterativo utilizado para resolver sistemas de ecuaciones lineales cuando la matriz `A` es simétrica y definida positiva. El algoritmo mejora la convergencia del **método de descenso** aplicando direcciones A-ortogonales, lo que le permite converger más rápidamente hacia la solución.

### 💡 **Proceso**

1. **Direcciones A-ortogonales**: El método genera direcciones de búsqueda que son A-ortogonales, es decir, que satisfacen `vᵀᵢ A vⱼ = 0` para `i ≠ j`.
2. **Iteraciones**: En cada paso, el algoritmo calcula el gradiente, obtiene una dirección A-ortogonal mediante el método de Gram-Schmidt, y actualiza la solución aproximada `x(k)`.

### 📋 **Ejercicios**  

#### **Ejercicio 1:**  
Implementar una función que reciba una lista de vectores y un vector `v`, y devuelva un vector `u` que sea el resultado de aplicar un paso de la modificación del método de Gram-Schmidt.  
Esta función se utiliza para obtener direcciones A-ortogonales, que son esenciales para el funcionamiento del método.

#### **Ejercicio 2:**  
Implementar el **método del gradiente conjugado**. La función debe recibir:
- Una matriz `A ∈ Rⁿˣⁿ`
- Un vector `b ∈ Rⁿ`
- Un vector inicial `x₀ ∈ Rⁿ`
- Un número `n` de iteraciones

El programa debe devolver:
- La aproximación `x(n)`
- Una lista con los errores \(\| b - A x(k) \|_2\) en cada paso

#### **Ejercicio 3:**  
Aplicar el **método del gradiente conjugado** en un sistema de ecuaciones donde:
- `A` es una matriz `10x10` definida como `A = Mᵀ M + I`, donde `M` es una matriz aleatoria de tamaño `10x10`
- `b` es un vector aleatorio de tamaño `10`
- `x₀` es un vector aleatorio de tamaño `10`
- Número de iteraciones: `N = 20`

Graficar los errores en función del número de pasos.

### 🛠️ **Tecnologías**
- **Python** 🐍
- **NumPy** para operaciones matriciales
- **Matplotlib** para graficar los errores

## 🔍 Notas
- El algoritmo de **gradiente conjugado** es adecuado para resolver sistemas de ecuaciones lineales cuando la matriz es simétrica y definida positiva.
- Los errores se miden con la norma 2: \(\| b - A x(k) \|_2\).
- El método converge más rápidamente que el **método de descenso** debido a la A-ortogonalidad de las direcciones generadas.

📩 **Contribuciones y sugerencias son bienvenidas!** 🚀
