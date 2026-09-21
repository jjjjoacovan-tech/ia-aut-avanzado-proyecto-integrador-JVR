IA AUT Avanzado — Proyecto Integrador
Repositorio para la segunda parte del curso IA AUT Avanzado (Coderhouse). Acá van a ir sumándose los checkpoints del proyecto integrador, desde M1 hasta M11.


Alumno: Joaquin Van Rompaey
Checkpoint 1 (M1) — Agente base de calificación de leads
Archivo: checkpoint1_joaquin_vanrompaey.json


Workflow de n8n con:


* Chat Trigger público como punto de entrada de la conversación.
* AI Agent (modo Tools Agent) conectado a su modelo de lenguaje mediante el nodo nativo Anthropic Chat Model.
* Guardrail de iteraciones: maxIterations: 7 (dentro del rango 5-10 pedido).
* System Message modular, estructurado en ROL → ÁMBITO → OBJETIVO → REGLAS Y ESCALAMIENTO, redactado en español rioplatense sin lenguaje inclusivo.
* Herramienta nativa conectada lateralmente al agente: Google Sheets Tool - Registrar Lead, con una descripción semántica extensa que le indica al modelo cuándo invocarla de forma autónoma (y cuándo no).
* Nodo de observabilidad: Slack - Reporte de Observabilidad, que postea al finalizar cada ejecución un log con la entrada del usuario, la respuesta del agente y la cantidad de pasos intermedios (herramientas invocadas).


El workflow fue probado en vivo dentro de n8n antes de exportarlo: ejecución de punta a punta con los 5 nodos en verde, incluyendo la escritura real del lead calificado en la planilla de Google Sheets conectada.
Nota sobre el modelo
La consigna sugiere "preferentemente GPT-4o o Claude 3.5 Sonnet". El agente está conectado, mediante el nodo nativo Anthropic Chat Model, a Claude Sonnet 5 (la versión vigente de Claude al momento de hacer este checkpoint). Se mantiene el proveedor y el tipo de nodo pedidos; solo cambia la versión del modelo por disponibilidad.
Cómo importar el workflow
1. En n8n: Workflows → Import from File y seleccionar checkpoint1_joaquin_vanrompaey.json.
2. Reemplazar los placeholders REEMPLAZAR_... por credenciales propias:
   * REEMPLAZAR_CREDENCIAL_ANTHROPIC → credencial de Anthropic API.
   * REEMPLAZAR_CREDENCIAL_GOOGLE_SHEETS → credencial de Google Sheets OAuth2.
   * REEMPLAZAR_ID_PLANILLA_GOOGLE_SHEETS → ID de una planilla propia con una hoja "Leads" y columnas: Nombre, Empresa, Necesidad, Categoria, Fecha, Resumen.
   * REEMPLAZAR_CREDENCIAL_SLACK / REEMPLAZAR_ID_CANAL_SLACK → credencial y canal de Slack propios.
3. Activar el Chat Trigger y probar desde el panel de chat de n8n.
Próximos checkpoints
Módulo
	Estado
	M1 — Agente base
	✅ Entregado
	M2
	Pendiente
	...
	Pendiente
	M11
	Pendiente
