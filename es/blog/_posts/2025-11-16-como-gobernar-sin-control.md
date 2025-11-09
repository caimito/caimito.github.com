---
layout: blog-es
title: "Cómo gobernar sin control"
tags:
  - es
  - sns-es
  - dev-advocate-es
---

Por Stephan Schwab el {{ page.date | date: "%d.%m.%Y" }}

## Lecciones de liderazgo desde el borde del caos técnico

Todo líder quiere dos cosas a la vez:

🔹 Estabilidad

🔹 Innovación

¿El problema? Estas dos tiran en direcciones opuestas.

Para obtener ambas, muchas organizaciones recurren al *control* — la ilusión de seguridad a través de procesos, reuniones y métricas.

Pero en software, el control rara vez trae estabilidad.

Suele sólo ralentizar el ciclo de retroalimentación hasta que el sistema falla en silencio.

---

### El control no es gobernanza

La gobernanza no se trata de saberlo todo.

Se trata de **asegurar que las cosas correctas se vuelvan visibles en el momento correcto**.

Control significa decirle a la gente qué hacer.

Gobernanza significa diseñar un sistema que *dice la verdad por sí mismo*.

En buenas organizaciones de ingeniería, esa verdad viene de datos, no de informes de estado:

* Las pruebas pasan o fallan.
* Los pipelines corren o se detienen.
* El monitoreo muestra la realidad en tiempo real.

Eso es gobernanza — no gestión.

---

### Reemplazar permiso con visibilidad

Un sistema de software saludable no necesita aprobación previa para cada cambio.

Necesita un pipeline que **detecta cambios malos automáticamente**.

| Mentalidad de control antigua              | Práctica de gobernanza moderna                           |
| ------------------------------------------ | -------------------------------------------------------- |
| "Revisemos todo manualmente"              | "Las pruebas automatizadas y controles protegen producción" |
| "Debemos conocer cada detalle"            | "Los dashboards muestran flujo, errores y disponibilidad" |
| "Aprobamos los lanzamientos"              | "Aprobamos el *proceso* que asegura lanzamientos seguros" |
| "Necesitamos reuniones para alinear"      | "Necesitamos sistemas que detecten desalineación temprano" |

La gobernanza no es un cuello de botella. Es una **red de sensores**.

---

### El trabajo real del CTO

El CTO que gobierna sin control no gestiona personas directamente.

Gestiona **retroalimentación**.

Su trabajo es asegurar que:

* Cada cambio tiene una señal rápida y automatizada.
* Las métricas de calidad son visibles para todos.
* La deuda técnica se rastrea como deuda financiera.
* Los equipos poseen sus resultados de principio a fin.

Si esos sistemas existen, la gobernanza sucede naturalmente — sin estructuras de comando.

---

### El dilema del Director General

Los directores generales a menudo confunden el silencio con estabilidad.

Ven la falta de ruido como señal de control.

Pero en software, **el silencio significa ceguera**.

La estabilidad real se ve ruidosa — pero no de la manera que la mayoría de los ejecutivos piensan.

Sí, las pruebas corren. Los builds se disparan. Los logs ruedan. Las alertas parpadean.

Pero esos son solo **señales**.

El ruido real es **humano**:

* Ingenieros cuestionando las suposiciones de los demás mientras hacen pairing o mobbing.
* Equipos proponiendo spikes — "probemos esto durante dos días y veamos qué aprendemos."
* Diseñadores desafiando restricciones técnicas.
* Desarrolladores debatiendo compensaciones abiertamente.
* Alguien diciendo "no entiendo esto" y tres personas deteniéndose para explicar.

(Y no, no "revisiones de código" — esas a menudo degeneran en vigilancia tóxica, otra falacia de control disfrazada de calidad.)

Así suena una cultura de ingeniería saludable.

No es caótica — es **turbulencia colaborativa**.

Los artefactos técnicos no crean el ruido.

**La gente hablando, cuestionando y experimentando** sí lo hace.

Cuando el liderazgo confunde esa energía con desorden e intenta silenciarla, mata el ciclo de retroalimentación.

El trabajo no es silenciar la conversación — es asegurar que esa energía se convierta en aprendizaje, decisiones y mejor software.

Y sí, eso significa: escribir código que se desecha. Pruebas que solo sirven para entender. Experimentos que no llevan a ninguna parte.

Eso no es desperdicio — es **pensar**.

Las conversaciones son solo la parte visible y audible. El verdadero pensamiento ocurre en el código mismo.

Quien exige "features rápidos" mientras dice "hablen entre ustedes" no ha entendido que crear *y* desechar software es el proceso de pensamiento, no una demora antes de la programación "real".

---

### Confiar, pero instrumentar

"Confiar" suena blando, pero es medible.

Un equipo que puede desplegar diez veces al día sin retrocesos está *gobernado*.

Un equipo que necesita cinco aprobaciones y tres comités para cada lanzamiento está *controlado* — y aún así inseguro.

La diferencia no es solo confianza — es **instrumentación**.

Automatiza los ciclos de retroalimentación (pruebas, monitoreo, controles de despliegue), no a las personas.

Libera a los ingenieros de realizar teatro de seguridad para que puedan enfocarse en el trabajo que realmente importa: pensar, diseñar, experimentar, colaborar.

La gobernanza escala a través de **arquitectura, automatización y responsabilidad**, no jerarquía.

---

### La paradoja del liderazgo moderno

Cuanto más intentas controlar a los ingenieros, menos entiendes lo que realmente está sucediendo.

Cuanto más confías e instrumentas el sistema, más claro se vuelve todo.

Así que deja de pedir informes.

Pide **evidencia** — en forma de logs, métricas y retroalimentación automatizada.

Y no introduzcas un marco de gestión que invada la libertad de los desarrolladores de crear e innovar.

Sí, muchos coaches de métodos y autores de frameworks estarán en desacuerdo. Su modelo de negocio depende de creer que el desarrollo de software es planificable como la manufactura.

Pero aquí está el punto crítico para los líderes:

**¿Qué enfoque entrega valor más rápido?**

Los frameworks ciertamente pueden revelar desperdicio y producir señales. Ese es su valor.

Pero no son una solución duradera para las malas prácticas de desarrollo de software.

Una vez que el framework ha hecho su trabajo y expuesto los problemas, se necesitan buenas prácticas de desarrollo — no más ceremonias.

Los marcos que dictan *cómo* trabajar — standups obligatorios, estimaciones de story points, seguimiento de velocidad, ceremonias de sprint — cuestan tiempo y dinero.

Cambian el enfoque de **entregar software** a **realizar proceso**.

Más importante aún: Aumentan tu riesgo, no lo reducen.

¿Por qué? Porque tratan el desarrollo de software como manufactura — con una separación limpia entre *preparar el trabajo* (planificación, estimación, diseño) y *hacer el trabajo* (codificar, probar, desplegar).

Pero el software no es una línea de ensamblaje.

**Descubrimiento y entrega son inseparables.**

No sabes qué estás construyendo hasta que empiezas a construirlo:

* Los requisitos se clarifican a través del código.
* La arquitectura emerge a través de la experimentación.
* El "trabajo" *es* el aprendizaje.

Cuando fuerzas a los desarrolladores a "terminar de pensar" antes de comenzar a codificar, no estás reduciendo riesgo — estás **retrasando la retroalimentación** hasta que es costoso actuar sobre ella.

Y eso te cuesta oportunidades de mercado mientras tus competidores entregan.

Los equipos que entregan valor más rápido no son los que tienen más ceremonias.
Son los que pueden entregar temprano y a menudo — porque su liderazgo invirtió en sistemas de retroalimentación, no en sobrecarga de procesos.

Y aquí está la realidad económica: **Con buenas prácticas e IA, se necesitan equipos más pequeños.**

Así como los desarrolladores ascendieron desde ensamblador a C, a Java/C# — cada paso les permitió trabajar en un nivel más alto de abstracción —, la IA los eleva aún más hoy.

Eso significa:

* Menos sobrecarga de coordinación entre equipos grandes.
* Colaboración más directa entre desarrolladores y expertos del dominio.
* Decisiones más rápidas porque hay menos intermediarios involucrados.

No se necesitan 50 desarrolladores coordinados a través de un framework.

Se necesitan 3-5 desarrolladores muy buenos con herramientas de IA, retroalimentación sólida y acceso directo a expertos de negocio y del dominio.

Eso no solo es más rápido — es **órdenes de magnitud más barato**.

Los frameworks prometen organizar equipos grandes.

Las buenas prácticas con IA hacen innecesarios los equipos grandes.

Este tipo de pensamiento — estratégico, arquitectónico, consciente del producto — se convierte en la parte más valiosa del trabajo de software.

---

#### Resumen

* Control es supervisión humana.
* Gobernanza es retroalimentación del sistema.

Si quieres estabilidad *y* velocidad, no aumentes el control — fortalece la retroalimentación.

Así es como gobiernas sin control.

<!-- Cross-language links intentionally omitted -->
