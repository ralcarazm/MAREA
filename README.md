# CREA · Conformidad de Recursos Educativos Abiertos

**CREA · Conformidad de Recursos Educativos Abiertos** es una herramienta web para evaluar la conformidad formal de recursos educativos abiertos (REA/OER). Su objetivo es ayudar a revisar si un recurso cumple condiciones básicas de apertura, reutilización, accesibilidad, descripción y preservación sin entrar en la valoración disciplinar, científica o pedagógica profunda del contenido.

## Versión

**1.0.0-beta.5**

## Motivación

Los recursos educativos abiertos no dependen solo de que el acceso sea gratuito. Para que un recurso pueda considerarse formalmente abierto debe contar con condiciones jurídicas, técnicas y descriptivas que permitan su conservación, reutilización, adaptación, remezcla y redistribución.

La herramienta parte de esa idea y propone una evaluación formal centrada en aspectos verificables:

- acceso gratuito;
- licencia abierta o verificable;
- posibilidad de ejercer las 5R;
- formato, editabilidad y portabilidad;
- metadatos descriptivos y educativos;
- accesibilidad básica;
- publicación estable y preservación;
- identificación de procedencia, versiones y lengua principal.

La herramienta no sustituye una revisión experta completa. Sirve como instrumento de autoevaluación y documentación de la conformidad formal de un recurso.

## Qué evalúa

La matriz se organiza en seis categorías:

| Categoría | Peso |
|---|---:|
| Identificación del recurso | 10 % |
| Acceso y licencia de uso | 25 % |
| Formato y reutilización | 25 % |
| Metadatos | 10 % |
| Accesibilidad | 20 % |
| Publicación y preservación | 10 % |

El peso final no depende del número de preguntas de cada categoría. Cada bloque se normaliza internamente y después se pondera según su peso.

## Funcionamiento exacto

La evaluación se realiza en dos fases.

### 1. Filtro de conformidad mínima

Antes de calcular una puntuación oficial, la herramienta comprueba si existen condiciones excluyentes. Si se detecta una de ellas, el resultado oficial pasa a ser **No REA** y la puntuación global aparece como **No aplicable**.

Las condiciones excluyentes principales son:

- acceso no gratuito;
- todos los derechos reservados;
- ausencia de licencia;
- licencia con cláusula ND;
- licencia cerrada o ausencia de licencia que impida ejercer las 5R;
- DRM o restricciones técnicas severas que impidan la reutilización.

En estos casos, la herramienta puede mostrar una puntuación diagnóstica orientativa, pero esa puntuación no se utiliza como certificación.

### 2. Puntuación ponderada

Si el recurso supera el filtro mínimo, la herramienta calcula una puntuación sobre 100. La puntuación se obtiene así:

1. Cada pregunta suma puntos dentro de su categoría.
2. La categoría se normaliza internamente.
3. El resultado se multiplica por el peso asignado a esa categoría.
4. La suma de las seis categorías da la puntuación final.

Los niveles de resultado son:

| Puntuación | Resultado |
|---:|---|
| 85–100 | Conformidad alta |
| 70–84 | Conformidad notable |
| 55–69 | Conformidad básica |
| 40–54 | Conformidad parcial |
| 0–39 | Conformidad baja |

Si hay una condición excluyente, el resultado es **No REA**. Si la licencia no puede verificarse automáticamente, el resultado es **No verificable como REA**.

## Reglas de coherencia

La herramienta incluye avisos automáticos para evitar combinaciones incoherentes de respuestas. Por ejemplo:

- Una licencia con **ND** no puede considerarse compatible con revisión, adaptación y remezcla.
- Una licencia con **NC** no se considera equivalente a 5R sin restricciones.
- Si el recurso no puede descargarse, el derecho de retener queda limitado.
- Si el recurso no es editable, la revisión, adaptación y remezcla quedan limitadas en la práctica.
- Si el recurso depende de una plataforma concreta, la portabilidad y preservación pueden verse afectadas.
- Si se selecciona una licencia institucional, educativa o propia no verificable, la herramienta solicita revisión manual.

Cuando procede, la aplicación ajusta automáticamente la respuesta sobre las 5R para reflejar barreras jurídicas o técnicas.

## Resultados generados

Después de validar el formulario, la herramienta muestra:

- resultado global;
- puntuación oficial o estado de no aplicabilidad;
- puntuación diagnóstica, si corresponde;
- puntuaciones parciales por categoría;
- avisos de exclusión o revisión manual;
- sello descargable en SVG;
- sello descargable en PNG;
- código HTML de inserción del sello.

El sello incluye:

- título de la herramienta;
- nivel alcanzado;
- puntuación;
- estrellas;
- fecha de evaluación;
- versión de la herramienta.

## Tecnologías

La herramienta está construida con tecnologías web estándar:

- HTML;
- CSS;
- JavaScript;
- Bootstrap 5.3.8;
- generación de SVG y PNG en el navegador.

## Estructura de archivos

```text
/
├── index.html
├── README.md
├── LICENSE.md
└── assets/
    └── css/
        └── styles.css
```

## Disponibilidad

La herramienta se encuentra disponible en

## Limitaciones

La herramienta evalúa conformidad formal. No evalúa:

- calidad científica del contenido;
- adecuación pedagógica profunda;
- exactitud disciplinar;
- eficacia didáctica;
- alineación curricular detallada;
- cumplimiento legal completo en contextos jurisdiccionales específicos.

Los resultados deben interpretarse como una evaluación formal automatizada y documentada, no como una certificación institucional externa.

## Créditos

Idea: **Rubén Alcaraz Martínez** y **Gema Santos Hermosa**, Universitat de Barcelona.  
Desarrollo: **Rubén Alcaraz Martínez**.

## Licencia

Este repositorio utiliza una licencia diferenciada para código y contenidos:

- **Código fuente:** GNU General Public License v3.0.
- **Matriz, textos y documentación:** Creative Commons Reconocimiento 4.0 Internacional (CC BY 4.0).