# Protocolo HALO
## Human-Anchored Labor Optimization

**Autor:** Alberth Rodríguez — puraIA  
**Licencia:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)  
**Versión:** 1.0.0  
**Contacto:** [linkedin.com/in/alberth-rodríguez-puraia](https://linkedin.com/in/alberth-rodríguez-puraia)

---

> *"La IA ejecuta mejor cuando un ser humano la dirige con precisión.  
> El ser humano trabaja mejor cuando la IA amplifica su criterio, no lo reemplaza.  
> Eso es HALO."*

---

## ¿Qué es el Protocolo HALO?

HALO es un protocolo de diseño de flujos de automatización IA donde **el ser humano es el nodo inteligente central**, no el elemento que se elimina.

Resuelve el problema más común en organizaciones que adoptan IA: conectar el caos directamente a la máquina. Solicitudes sin filtrar, contexto inflado, agentes sin supervisión, outputs sin responsable. El resultado: gasto excesivo en tokens, errores sin accountability y destrucción de empleo innecesaria.

HALO invierte ese patrón. Coloca a una persona — el **HiR (Human Intelligence Router)** — entre la solicitud y el agente IA. Esa persona lee, filtra, comprime y enruta. El agente recibe instrucciones precisas. El resultado mejora. El costo cae. El humano tiene un rol real y calificado.

---

## El problema que HALO resuelve

| Sin HALO | Con HALO |
|----------|----------|
| Agente recibe correo completo (~2.000 tokens) | HiR extrae la tarea (~150 tokens) |
| Output genérico, fuera de contexto | Output preciso, calibrado al cliente |
| Nadie firma el resultado | HiR valida y firma cada entregable |
| Personal desplazado sin reconversión | Personal reconvertido al rol HiR |
| Gasto en tokens sin control ni métricas | Reducción documentada del 40–80% |

---

## Las 4 capas del flujo HALO

```
┌─────────────────────────────────────────────┐
│  CAPA 1 — Entrada bruta                     │
│  Clientes · ERP · Correo · Bases de datos   │
│  ⚠ NUNCA conectar directo a un agente IA    │
└──────────────────┬──────────────────────────┘
                   │ solicitud sin filtrar
                   ▼
┌─────────────────────────────────────────────┐
│  CAPA 2 — Nodo HiR ★ CENTRO DEL SISTEMA    │
│  Lee · Filtra · Comprime · Clasifica        │
│  Selecciona agente · Construye prompt       │
│  Valida output · Registra el caso           │
└──────────────────┬──────────────────────────┘
                   │ prompt optimizado (<600 tokens)
                   ▼
┌─────────────────────────────────────────────┐
│  CAPA 3 — Agentes IA especializados         │
│  AG-RED-01 · AG-ANA-01 · AG-COD-01          │
│  AG-INV-01 · AG-CLA-01                      │
│  Solo reciben inputs estructurados          │
└──────────────────┬──────────────────────────┘
                   │ output del agente
                   ▼
┌─────────────────────────────────────────────┐
│  CAPA 4 — Output validado                   │
│  Revisado por HiR · Metadata de trazabilidad│
│  Entregado con responsable identificado     │
└─────────────────────────────────────────────┘
```

---

## El rol HiR — Human Intelligence Router

El HiR es el cargo que HALO crea. No es un programador. No es un prompt engineer. Es el nodo humano que hace que todo el sistema funcione mejor.

**Responsabilidades:**
- Leer la solicitud completa y extraer la intención real
- Eliminar contexto irrelevante antes de activar cualquier agente
- Seleccionar el agente correcto del catálogo
- Construir el prompt usando la Plantilla HALO
- Revisar el output antes de entregarlo
- Registrar el caso en el log de aprendizaje

**¿Quién puede ser HiR?**  
Cualquier persona con comprensión del negocio, capacidad de síntesis escrita y disposición a aprender el protocolo. No requiere formación técnica. Capacitación estimada: 10–20 horas.

**Plan de carrera:**

| Nivel | Rol | Alcance |
|-------|-----|---------|
| Nivel 1 | HiR Junior | Gestiona agentes de redacción y clasificación |
| Nivel 2 | HiR Senior | Gestiona todos los agentes, forma nuevos HiRs |
| Nivel 3 | Arquitecto HALO | Diseña flujos, configura agentes para clientes |

---

## La Plantilla HALO — estructura de prompts

Todo prompt enviado a un agente IA debe completar estos 5 campos:

```
ROL:           [Quién es el agente en ESTE contexto específico]
TAREA:         [Una sola tarea. Una oración. Sin ambigüedad.]
CONTEXTO:      [Solo lo indispensable. Máximo 5 oraciones.]
RESTRICCIONES: [Qué NO debe hacer. Mínimo 2 restricciones.]
FORMATO:       [Estructura exacta: secciones, extensión, estilo]
```

> **Regla de los 600 tokens:** Si el prompt supera los 600 tokens de entrada, volver al campo CONTEXTO y eliminar información hasta cumplir el límite.

**Ejemplo aplicado:**

```
ROL: Eres un redactor de comunicaciones corporativas en español
     para una empresa de logística centroamericana.

TAREA: Redacta un correo de disculpa al cliente por retraso
       de 3 días en el pedido #4821.

CONTEXTO: Cliente empresa mediana de retail, relación desde 2019.
          Retraso por paro de transportistas (fuerza mayor).
          Buen historial de pago. Sin incidentes previos.

RESTRICCIONES: No ofrecer descuentos ni compensaciones económicas.
               No mencionar detalles internos de la operación.
               Tono formal pero empático.

FORMATO: Asunto + saludo + cuerpo de 3 párrafos máx + despedida.
         Total: no más de 150 palabras.
```

---

## Árbol de decisión HiR

```
PASO 1: ¿La tarea realmente necesita IA?
        NO → Resolver directamente. No activar ningún agente.
        SÍ → Continuar al paso 2.

PASO 2: ¿Qué tipo de output se necesita?
        Texto estructurado    → AG-RED-01
        Análisis de datos     → AG-ANA-01
        Código                → AG-COD-01
        Síntesis información  → AG-INV-01
        Clasificación rápida  → AG-CLA-01
        Tarea compuesta       → Dividir. Una llamada por agente, en secuencia.

PASO 3: ¿Tengo todos los inputs requeridos?
        NO → Pedir la información faltante ANTES de llamar al agente.
        SÍ → Construir prompt con la Plantilla HALO.

PASO 4: ¿El output es entregable?
        SÍ                  → Añadir metadata y entregar.
        NO (menor)          → Corregir directamente.
        NO (significativo)  → Ajustar el prompt. Rellamar al agente.
        FALLO CRÍTICO       → Escalar a humano senior. Nunca entregar incorrecto.
```

---

## Catálogo base de agentes

| ID | Función | Inputs requeridos | Benchmark |
|----|---------|-------------------|-----------|
| AG-RED-01 | Redacción de documentos | tema, tono, audiencia, extensión, restricciones | 200–400 tokens entrada |
| AG-ANA-01 | Análisis de datos | dataset reducido, pregunta específica, formato output | 300–600 tokens entrada |
| AG-COD-01 | Generación de código | lenguaje, función, restricciones técnicas, contexto mínimo | 200–500 tokens entrada |
| AG-INV-01 | Research y síntesis | pregunta, alcance, fuentes, formato entrega | 150–300 tokens entrada |
| AG-CLA-01 | Clasificación de inputs | ítem a clasificar, categorías, criterio de decisión | 100–200 tokens entrada |

---

## Las 5 dimensiones de madurez HALO

| # | Dimensión | Qué evalúa |
|---|-----------|-----------|
| D1 | Nodo HiR | ¿Hay un humano activo y entrenado en cada flujo de IA? |
| D2 | Eficiencia de tokens | ¿El consumo está optimizado? ¿Se mide el costo mensual? |
| D3 | Trazabilidad | ¿Cada output tiene responsable, agente y fecha identificados? |
| D4 | Impacto en empleo | ¿La automatización creó o transformó roles en vez de eliminarlos? |
| D5 | Ciclo de mejora | ¿El sistema aprende? ¿Existe biblioteca de prompts activa? |

**Escala de Madurez HALO Global (suma D1–D5, máx. 25 puntos):**

| Puntaje | Nivel | Descripción |
|---------|-------|-------------|
| 0–7 | HALO Crítico | Automatización sin control. Riesgo alto. |
| 8–14 | HALO Inicial | Automatización sin diseño. Riesgo moderado. |
| 15–20 | HALO en Desarrollo | Bases presentes. Brechas importantes. |
| 21–25 | HALO Avanzado | Sistema bien diseñado. Optimización fina. |

---

## Los 6 principios del Protocolo HALO

1. Ningún agente IA recibe una solicitud sin haber pasado por un filtro humano (HiR).
2. Los agentes IA son herramientas especializadas, no generalistas autónomos.
3. Un prompt bien construido por un humano vale más que 10 llamadas de un agente autónomo.
4. La trazabilidad humana es un activo legal y competitivo, no un obstáculo.
5. El ahorro de tokens es ahorro de dinero, tiempo y energía — los tres son recursos finitos.
6. Cada workflow implementado debe generar un rol HiR, no eliminarlo.

---

## Glosario

| Término | Definición |
|---------|-----------|
| **HALO** | Human-Anchored Labor Optimization. El protocolo completo. |
| **HiR** | Human Intelligence Router. El rol humano central del sistema. |
| **Token** | Unidad de procesamiento de LLMs. ~4 caracteres / ~0.75 palabras en español. |
| **Contexto inflado** | Prompt con información irrelevante que aumenta el costo sin mejorar el output. |
| **Plantilla HALO** | Estructura de 5 campos para construir prompts optimizados. |
| **Scorecard HALO** | Herramienta de medición de las 5 dimensiones. Escala 1–5 por dimensión. |
| **Madurez HALO** | Nivel global del sistema: Crítico · Inicial · En Desarrollo · Avanzado. |
| **Sello HALO™** | Certificación exclusiva de puraIA. **No cubierta por esta licencia.** |
| **Biblioteca de prompts** | Repositorio de prompts validados por tipo de tarea. |
| **Log de aprendizaje** | Registro de interacciones: agente, prompt, output, correcciones. |

---

## Cómo contribuir

1. Abre un **Issue** describiendo la mejora y el problema que resuelve.
2. Para contribuciones mayores, abre un **Pull Request** con el texto propuesto.
3. Toda contribución se distribuye bajo la misma licencia **CC BY-SA 4.0**.
4. Los contribuidores significativos se reconocen en `CHANGELOG.md`.

**Áreas prioritarias:**
- Traducciones (inglés y portugués primero)
- Casos de implementación anonimizados
- Extensiones sectoriales (salud, educación, finanzas, gobierno)
- Mejoras a la Plantilla HALO basadas en implementaciones reales

---

## Licencia

**Protocolo HALO © 2025 Alberth Rodríguez, puraIA**

Licenciado bajo [Creative Commons Atribución-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

✅ Puede usar, compartir y adaptar este protocolo para cualquier propósito, incluso comercial.  
✅ Puede construir servicios basados en el protocolo.  
⚠ Debe citar al autor: **Alberth Rodríguez — puraIA** con enlace a este repositorio.  
⚠ Debe distribuir sus adaptaciones bajo la misma licencia CC BY-SA 4.0.  
🚫 **El Sello HALO™ y los instrumentos de auditoría son propiedad exclusiva de puraIA y NO están incluidos en esta licencia.**

---

## Certificación oficial

¿Tu organización implementó HALO y quiere el **Sello HALO™ Certificado**?  
La certificación oficial — incluyendo el diagnóstico con instrumentos propietarios y la garantía de resultados — está disponible a través de **puraIA**.

**Contacto:** [linkedin.com/in/alberth-rodríguez-puraia](https://linkedin.com/in/alberth-rodríguez-puraia)

---

*Protocolo HALO v1.0.0 · CC BY-SA 4.0 · puraIA · Costa Rica · 2025*
