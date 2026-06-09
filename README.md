# Simulador del Protocolo ALOHA de Canal Compartido

Este proyecto es una aplicación web interactiva diseñada para simular y analizar el comportamiento del protocolo de acceso al medio **ALOHA** en un entorno de red simplificado con 3 nodos independientes que compiten por un único canal de transmisión común.

La interfaz cuenta con soporte nativo para **Modo Claro** y **Modo Oscuro**, optimización de rendimiento visual y persistencia de configuración de tema a través del navegador.

---

## Características Principales

* **Modelo de Canales Dinámicos:** Eliminación de estados ociosos (*idle*) para evaluar de manera crítica únicamente escenarios de rendimiento real bajo demanda constante.
* **Diseño de Panel Dividido (Layout de 2 Columnas):** Panel izquierdo enfocado en la configuración de parámetros y monitorización de nodos en tiempo real; panel derecho dedicado al registro secuencial de eventos y métricas globales.
* **Control de Variables en Tiempo Real:** * Ajuste de la probabilidad de transmisión ($p$) de forma individual por ranura de tiempo.
    * Configuración flexible de la cantidad de *Time-slots* (ranuras de tiempo) a simular.
* **Modo Claro / Oscuro Nativo:** Interfaz adaptable con guardado automático de preferencia mediante `localStorage`.
* **Registro Automatizado con Alta Legibilidad:** Formato estandarizado en el historial donde la prioridad semántica define estrictamente cada ranura como **transmisión exitosa** o **colisión**.

---

## Parámetros de Simulación y Métricas

El simulador computa y despliega de manera automática los siguientes indicadores de rendimiento al finalizar cada ejecución:

| Métrica | Descripción |
| :--- | :--- |
| **Slots** | Cantidad total de intervalos de tiempo evaluados en la sesión actual. |
| **Transmisiones Exitosas** | Slots de tiempo en los que exactamente un único nodo transmitió sin interferencias. |
| **Colisiones** | Slots en los que dos o más nodos intentaron transmitir en simultáneo, corrompiendo la señal. |
| **Eficiencia** | Porcentaje de éxito crítico del canal respecto al total de slots configurados ($\frac{\text{Éxitos}}{\text{Slots}} \times 100$). |

---

## Tecnologías Utilizadas

* **HTML5:** Estructuración semántica y accesibilidad garantizada mediante atributos `sr-only`.
* **CSS3 (Grid, Flexbox y Variables):** Arquitectura responsiva de dos columnas con transiciones fluidas de color para la alternancia de temas.
* **JavaScript (ES6+):** Motor lógico asíncrono basado en temporizadores (`setTimeout`) para recrear visualmente el procesamiento ranura por ranura.

---

## 🚀 Instrucciones de Uso

1.  Descarga o clona el archivo `aloha_simulator_modern.html`.
2.  Abre el archivo directamente en cualquier navegador web moderno (Chrome, Firefox, Edge, Safari).
3.  (Opcional) Usa el botón **Modo Oscuro / Modo Claro** en la esquina superior derecha para ajustar el contraste visual de tu preferencia.
4.  Ajusta la **Probabilidad de transmisión ($p$)** y la cantidad de **Time-slots** utilizando los deslizadores numéricos.
5.  Haz clic en el botón central **Iniciar simulación** para observar el comportamiento en tiempo real de los nodos y el llenado del registro de eventos.
