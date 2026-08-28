# 🌊🌱🔥 WEF-Game (Water, Earth, Fire)

> **Trabajo Práctico Integrador**  
> **Asignatura:** Programación Orientada a Objetos  
> **Carrera:** Ingeniería en Sistemas de Información  
> **Institución:** Universidad Adventista del Plata (UAP)  
> **Fecha límite de entrega:** 28/09/2026  

---

## 📖 1. Introducción

**WEF-Game** es un juego por turnos basado en la mecánica clásica de *Piedra–Papel–Tijera*, adaptado a un sistema estratégico de elementos con vida y daño configurable:

* 💧 **Agua**
* 🌱 **Tierra**
* 🔥 **Fuego**

A diferencia del juego tradicional, cada jugador dispone de un conjunto de unidades/cartas elementales, cada una con un nivel de energía (vida al 100%). En cada ronda, los elementos se enfrentan y se aplican daños basados en la interacción de tipos hasta que uno de los jugadores se quede sin unidades disponibles.

---

## 🎮 2. Mecánica del Juego

* **Modalidad:** Partida 1 vs 1 entre un **Jugador Humano** y una **Inteligencia Artificial (IA)**.
* **Mazo Inicial:** Cada jugador recibe un conjunto de $N$ elementos (por defecto 5 o 6) asignados de forma aleatoria con **100% de energía inicial**.
* **Desarrollo de Rondas:**
  1. El jugador humano y la IA seleccionan un elemento disponible de su equipo.
  2. Los elementos se enfrentan en combate.
  3. Cada elemento realiza un ataque que reduce la energía del adversario según la matriz de efectividad.
  4. Si la energía de un elemento llega a **0%**, queda **fuera de combate** y debe ser reemplazado por otro elemento disponible del mazo.
* **Condición de Victoria:** Gana el jugador que mantenga al menos un elemento con energía mientras el oponente se queda sin unidades activas.

---

## ⚔️ 3. Sistema de Daño y Efectividad

El sistema cuenta con una matriz configurable de efectividad de daño entre tipos de elementos, permitiendo modificar las reglas de daño sin alterar la lógica principal del juego.

### Ejemplo de Configuración de Daño

| Atacante | Defensor | Daño Infligido |
| :--- | :--- | :--- |
| 💧 **Agua** | 🔥 **Fuego** | 50% |
| 🌱 **Tierra** | 🔥 **Fuego** | 20% |
| 🔥 **Fuego** | 🌱 **Tierra** | 40% |
| 💧 **Agua** | 🌱 **Tierra** | 30% |

---

## 🤖 4. Tipos de Inteligencia Artificial

El juego contempla distintos niveles de IA para el oponente, los cuales pueden seleccionarse o asignarse aleatoriamente:

1. **🎲 IA Aleatoria:**
   * Selecciona un elemento al azar entre los disponibles, sin evaluar ventajas de tipo ni estado de la partida.
2. **🧠 IA Estratégica:**
   * Evalúa el elemento del oponente y selecciona el elemento propio que otorgue la mayor ventaja (maximizando el daño infligido y minimizando el recibido).
3. **⚡ Super IA (Estrategia + Eficiencia):**
   * Maximiza la ventaja frente al oponente optimizando el uso de recursos (por ejemplo, si al rival le resta 20% de vida, puede priorizar un elemento que garantice la eliminación sin desperdiciar unidades críticas).

---

## 🏛️ 5. Principios de Diseño y Restricciones de POO

El proyecto debe validar el modelo propuesto y respetar rigurosamente las buenas prácticas de la Programación Orientada a Objetos:

### 🚫 Restricciones Obligatorias
* ❌ **No se permite lógica centralizada en una sola clase** *(evitar God Classes / clases monolíticas)*.
* ❌ **No se permite resolver interacciones con múltiples `if` o `switch`** *(utilizar polimorfismo, Double Dispatch, matrices de daño o patrones de diseño)*.
* ❌ **No se permite el uso de estructuras sin encapsulación** *(todos los atributos deben proteger su estado mediante modificadores de acceso y métodos adecuados)*.
* ❌ **No se permite resolver el sistema como funciones globales** *(todo comportamiento debe residir en objetos y clases cohesivas)*.

---

## 👥 6. Información del Grupo y Entrega

* **Modalidad:** Grupos de 2 a 3 personas.
* **Formato de Entrega:** Archivo comprimido subido al campus virtual por un integrante del grupo antes del **28/09/2026**.

### Integrantes
* Eric Sand (*completar con integrantes del grupo*)
