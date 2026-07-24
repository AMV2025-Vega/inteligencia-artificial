# Actividad de Clase: Análisis de un agente de IA en Hugging Face Spaces

## 1. Nombre del Space

**Nombre:** Gemma 4 Vision Token Budget

**Enlace:** https://huggingface.co/spaces/google/gemma4_vision_token_budget

---

## 2. ¿Qué hace el agente?

 Este Space permite subir una imagen y cambiar el presupuesto de tokens de visión para observar cómo esto afecta el análisis que realiza el modelo. De esta forma, el usuario puede comparar los resultados y entender cómo influye esa configuración en el procesamiento de la imagen.
---

## 3. Análisis PEAS

| Elemento        | Respuesta                                                                                                                            |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| **Performance** | Analizar correctamente la imagen y mostrar un resultado útil para que el usuario pueda comparar el efecto del presupuesto de tokens. |
| **Environment** | Interactúa con el usuario, la imagen cargada y la interfaz del Space.                                                                |
| **Actuators**   | Genera una descripción o análisis de la imagen y muestra el resultado según la configuración elegida.                                |
| **Sensors**     | Recibe la imagen subida por el usuario y el presupuesto de tokens seleccionado.                                                      |

---

## 4. Clasificación del entorno

| Propiedad | Clasificación | Justificación |
|-----------|---------------|---------------|
| **Observable** | Total | El agente recibe toda la imagen que el usuario le proporciona para realizar el análisis. |
| **Determinista** | Sí | Si se utiliza la misma imagen y la misma configuración, el comportamiento esperado es el mismo. |
| **Episódico** | Sí | Cada análisis es independiente del anterior. Una imagen no afecta el resultado de la siguiente. |
| **Estático** | Sí | La imagen permanece igual mientras el agente la procesa. |
| **Discreto** | Sí | Tanto las entradas como las salidas son eventos definidos: se envía una imagen y se obtiene un resultado. |
| **Conocido** | Sí | La tarea que debe realizar el agente y el tipo de información que recibe son conocidos desde el inicio. |

---

## 5. ¿Qué tipo de programa de agente creen que es?

**Tipo de agente:** Agente basado en objetivos.

**Justificación:**

Considero que es un agente basado en objetivos porque su comportamiento está orientado a cumplir una tarea específica: analizar una imagen y mostrar cómo cambia el resultado al modificar el presupuesto de tokens. El usuario puede cambiar la configuración y el agente adapta su respuesta para seguir cumpliendo ese objetivo.

No es posible asegurar cómo está implementado internamente solo observando el Space. Podría utilizar un modelo entrenado con aprendizaje automático o incluso otro tipo de implementación. La clasificación se basa únicamente en el comportamiento que se observa desde la interfaz.
 
---

# Reto adicional

## 1. Totalmente observable, determinista y episódico

**Space:** Gemma 4 Vision Token Budget.

**Justificación:**

El agente recibe toda la información necesaria (la imagen), procesa cada solicitud de forma independiente y, usando la misma configuración, se espera obtener el mismo resultado.

## 2. Parcialmente observable, estocástico y secuencial

**Ejemplo:** Un chatbot conversacional de Hugging Face.

**Justificación:**

- **Parcialmente observable:** el agente solo conoce la información que el usuario decide escribir.
- **Estocástico:** una misma pregunta puede generar respuestas diferentes.
- **Secuencial:** cada respuesta depende del historial de la conversación.
