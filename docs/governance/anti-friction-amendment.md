# CornerTech AI | Governance Anti-Friction Amendment

**RFC CTAI-GOV-AF-001 · contenido v0.1 aprobado por el Founder · 16 noviembre 2026 · Asia/Dubai**  
**Decisión:** FOUNDER APPROVED (contenido de la enmienda). **Integración al repositorio corporativo: PENDIENTE**. Esta aprobación no es GO para push, PR, merge, deploy, cambios de servicio, permisos ni otros efectos.  
**Uso:** fuente aprobada para preparar el cambio mínimo a `Conquereleven/cornertech-ai`; la evidencia de 3L y el encargo de la sección 8 son históricos/operativos y **no constituyen instrucciones automáticas para ejecutar** cuando este documento sea integrado.  
**Responsable del análisis:** ChatGPT, coordinación y autocrítica; **decisor:** Founder & CEO de CornerTech AI.  
**Proyecto de evidencia:** 3L Pastelerías Dubai; **aplicación propuesta:** gobernanza corporativa, con adopción local independiente cuando proceda.

## 1. Decisión ejecutiva propuesta

**Diagnóstico:** las demoras recurrentes no provienen de ausencia de governance, sino de su aplicación defectuosa por parte del asistente: solicitudes duplicadas de GO, confusión entre control y trabajo, handoffs redundantes, falta de tareas ejecutables, verificación tardía de herramientas disponibles y afirmaciones prematuras de éxito.

**Propuesta:** incorporar un anexo corto de ejecución sin fricción a la gobernanza corporativa, sin reescribir de momento Execution Standard 1.0, CT-WCOS v1.1 ni AMAE v0.1. Una vez aprobado, integrarlo en el documento canónico que el Founder designe y validar su adopción con una sesión nueva. No duplicar el estándar completo dentro de 3L.

**No se propone:** relajar autorizaciones de push/PR/merge/deploy, gastar recursos, acceder a secretos, cambiar Railway, enviar comunicaciones ni usar datos de clientes. «Autonomía» significa actuar dentro del alcance autorizado, no ampliar el alcance.

## 2. Fuentes y estado de autoridad

**Fuentes primarias inspeccionadas, versión fijada en GitHub:** `Conquereleven/cornertech-ai`, `main` en `d8275e90e35c90e4c293efd179f89c69a60de75d` (commit del 9 noviembre 2026):

- `docs/governance/execution-standard.md`: Execution Standard 1.0. Exige resultado, estado PREPARED/EXECUTED/VERIFIED/CLOSED o BLOCKED, reutilizar evidencia y usar el reporte más pequeño que sostenga la decisión.
- `docs/governance/world-class-operating-standard.md`: CT-WCOS v1.1 + 9D. Exige resultado inspeccionable, ejecución segura dentro del GO, proporcionalidad del análisis y «One control. One evidence. One approval».
- `docs/governance/adaptive-multi-agent-engineering.md`: AMAE v0.1. Exige un DRI, SOLO/DUAL/SPECIALIZED proporcional y ningún gate/ticket nuevo por incorporar agentes. El texto inspeccionado figura como Founder-approved, con adopción de repo pendiente en esa revisión: no confundir aprobación de dirección con activación técnica.
- `docs/security/permissions.md`: regla general de lectura permitida, acciones sensibles con confirmación y acciones destructivas prohibidas. Las exclusiones específicas del Founder siguen prevaleciendo.
- `docs/security/human-in-the-loop.md`: aprobaciones humanas antes de acciones sensibles.

**Actualización comprobada para integración (16 noviembre 2026):** el PR corporativo [#111](https://github.com/Conquereleven/cornertech-ai/pull/111) figura **MERGED** en GitHub y `main` se consultó en `d8275e90e35c90e4c293efd179f89c69a60de75d`. El texto sobre AMAE pendiente describe el estado en la revisión histórica del RFC, no su estado remoto actual. La carga de instrucciones en cada agente o repositorio cliente sigue requiriendo evidencia propia.

**Enlaces de consulta:** [Execution Standard 1.0](https://github.com/Conquereleven/cornertech-ai/blob/d8275e90e35c90e4c293efd179f89c69a60de75d/docs/governance/execution-standard.md) · [CT-WCOS v1.1](https://github.com/Conquereleven/cornertech-ai/blob/d8275e90e35c90e4c293efd179f89c69a60de75d/docs/governance/world-class-operating-standard.md) · [AMAE v0.1](https://github.com/Conquereleven/cornertech-ai/blob/d8275e90e35c90e4c293efd179f89c69a60de75d/docs/governance/adaptive-multi-agent-engineering.md) · [Permissions](https://github.com/Conquereleven/cornertech-ai/blob/d8275e90e35c90e4c293efd179f89c69a60de75d/docs/security/permissions.md) · [Human-in-the-Loop](https://github.com/Conquereleven/cornertech-ai/blob/d8275e90e35c90e4c293efd179f89c69a60de75d/docs/security/human-in-the-loop.md).

**Contexto 3L inspeccionado:** `Conquereleven/tres-leches-demo` `main` en `13c46096087a7e58caecb8e2625bc4fc34e73e7a`; `AGENTS.md` del repo; [PR #70](https://github.com/Conquereleven/tres-leches-demo/pull/70) y [PR #77](https://github.com/Conquereleven/tres-leches-demo/pull/77), ambos **Draft** al revisar. Esos PR no equivalen a adopción en `main`. La fuente del servicio Railway Production fue consultada en lectura el 16 noviembre 2026: repo 3L, rama `main`, SHA `13c4609`, servicio `live`, sin staged changes. La política específica de PR preview/entornos efímeros no fue expuesta por esa lectura y permanece **UNKNOWN**.

## 3. Registro de diez fallos observados y regla correctiva

| ID | Fallo atribuible al asistente o al proceso coordinado | Evidencia en 3L/Hermes | Corrección propuesta |
|---|---|---|---|
| AF-01 | Responder con análisis o disculpas sin dejar trabajo ejecutable. | Tras reconocer burocracia, no se entregó el siguiente encargo. | **Action-first:** para tareas con GO y entorno ejecutor conocido, entregar o ejecutar una acción concreta en ese turno. |
| AF-02 | Pedir nuevamente un GO ya otorgado. | Push + un Draft PR ya autorizados; se intentó abrir otro ciclo de permiso. | **GO ledger:** registrar objeto, alcance, efectos y exclusiones; reutilizar autorización válida exactamente para ese efecto. |
| AF-03 | Convertir una incertidumbre limitada en bloqueo total. | Falta de visibilidad sobre PR previews detuvo también el push de rama; controles pueden separarse. | **Ejecución por efectos:** avanzar la parte reversibile y autorizada cuando su seguridad esté acreditada; bloquear sólo el efecto pendiente. |
| AF-04 | Crear handoffs, ZIP y recibos por cada comprobación. | Múltiples archivos de continuidad para un mismo gate de Railway. | **Un registro vivo:** actualizar issue/PR/handoff existente; nuevo documento sólo si cambia una decisión material o hay necesidad real de portabilidad. |
| AF-05 | Presentar enlaces o artefactos sin verificar contenido/ruta accesible. | Se ofrecieron descargas en respuestas previas sin acreditar suficientemente el archivo al momento de la afirmación. | **Artifact truth gate:** confirmar existencia exacta, integridad básica y acceso antes de anunciar «descargar». |
| AF-06 | Declarar un cambio de estado a partir de intención o selección de menú. | Hermes mostró «No change» y K2 seguía activo tras intentar restaurar OpenAI. | **Estado observado:** distinguir «seleccionado», «guardado», «funciona» y «verificado en el destino». |
| AF-07 | Tratar «sin prueba» como «probablemente seguro» o «seguro» indistintamente. | Se identificaron workflows sin deploy y origen Railway `main`, pero faltaba política de PR previews. | **Etiquetas de certeza:** VERIFIED, REPORTED, INFERRED, UNKNOWN; desconocido material sólo bloquea su efecto real. |
| AF-08 | Convertir al Founder en mensajero entre agentes y aplicaciones. | Solicitudes reiteradas de capturas/GO pese a existir conectores o evidencia ya disponible. | **Coordinator-first:** usar herramientas read-only existentes dentro de permisos; si falta acceso, pedir una sola decisión precisa. |
| AF-09 | Repetir pruebas y reauditorías sin un delta que las justifique. | Suite de 908 pruebas ya reportada; revisiones sucesivas sobre el mismo SHA. | **Delta-based verification:** reusar PASS del SHA exacto; ejecutar sólo tests faltantes o invalidados por cambios. |
| AF-10 | Desviar el foco del proyecto o del resultado empresarial. | La integración IFM/Hermes desplazó temporalmente el trabajo P0/P1 de 3L. | **Workspace anchor:** fijar cliente, outcome, DRI, siguiente entrega y presupuesto de interrupción; separar investigación de plataforma. |

Las descripciones anteriores combinan hechos de esta conversación, salidas reportadas por Hermes y verificaciones actuales de GitHub/Railway. **No son un informe de incidentes de Production**, ni atribuyen a Hermes acciones que no ejecutó. En particular, Hermes **detuvo correctamente** el push ante la condición literal de su encargo; el fallo de coordinación principal fue imponerle un criterio poco proporcional y no suministrar un camino de avance acotado.

## 4. Cláusulas operativas aprobadas en contenido (integración técnica pendiente)

**AF-R1 · Resultado por turno.** Cuando existe GO y herramienta/entorno capaz, el coordinador ejecuta la acción dentro del turno. Si no accede al entorno del usuario, entrega **un único encargo pegable**, con resultado esperado, verificaciones y límites. Un diagnóstico aislado no satisface una solicitud de implementación.

**AF-R2 · Ledger de permisos por efecto.** Mantener en el mismo issue/PR una tabla mínima: `acción`, `recurso`, `entorno`, `GO`, `exclusiones`, `estado`. No pedir repetidamente el GO para el mismo alcance. Tampoco extenderlo a otro efecto: push ≠ PR ≠ merge ≠ deploy ≠ cambios de datos o infraestructura.

**AF-R3 · Progreso seguro sin bypass.** Frente a incertidumbre, separar acciones técnicas por efecto y ejecutar sólo las que ya tienen evidencia de seguridad y GO. Ejemplo: un push no forzado a rama de revisión puede ser separable de abrir PR si la política de previews de PR es desconocida. Ante un trigger que pudiera afectar Production, mantener HOLD para esa acción.

**AF-R4 · Evidence reuse.** Antes de reejecutar tests, releer el SHA, la matriz de pruebas y el review existente. Un cambio en el código, entorno o criterio material puede invalidar evidencia; en ese caso ejecutar la mínima prueba de regresión apropiada. Una revisión independiente debe especificar quién revisó qué SHA.

**AF-R5 · Cero teatro documental.** Un trabajo conserva un único registro de continuidad. No crear un ZIP, informe o nueva «task» salvo que sea un entregable pedido, un gate material o un handoff necesario para que el siguiente ejecutor actúe. El recibo de cinco líneas no se convierte en segundo informe.

**AF-R6 · Certeza explícita.** `VERIFIED` se reserva para comprobaciones reales del objeto y entorno declarados. Respuestas de un agente, capturas, CI o ramas locales son `REPORTED` o `VERIFIED LOCAL` según su evidencia; no sustituyen Production. No inventar URLs, rutas, SHA, configuraciones o capacidades.

**AF-R7 · Inspección mínima y permisos.** Priorizar metadatos read-only y conectores existentes cuando las normas y el GO no lo prohíban. **No elevar** permisos para escrituras, secretos, datos de clientes, gastos ni infraestructura. Si un alcance específico prohíbe la consulta, respetarlo y pedir sólo ese permiso concreto cuando sea indispensable.

**AF-R8 · Un DRI y cierre por aceptación.** Elegir AMAE SOLO, DUAL o SPECIALIZED por riesgo y capacidades verificadas. No forzar un par de agentes ni repasar toda la auditoría si ya hay revisión válida. `CLOSED` exige comportamiento comprobado, aceptación y registro de pendientes.

**AF-R9 · Truth gate de archivos.** Antes de emitir un enlace descargable, comprobar que el archivo existe en la ruta actual, es legible, contiene lo prometido y su extensión coincide. Si falla, informar en vez de mostrar un enlace ficticio.

**AF-R10 · Brevedad ejecutable.** El reporte al Founder debe comenzar por resultado, riesgo y siguiente acción. No convertir estándares, nueve dimensiones o cinco líneas en diez formularios. El trabajo de producto y clientes sigue siendo la prioridad.

## 5. Ejemplo aplicado: 3L P0/P1, publicación sin Production

**Objetivo vigente:** publicar para revisión los seis commits locales que culminan en `06b94653e4cbe5e46fd4ef98bff5f45399ce1c85`, sobre la rama `local/payment-time-fulfillment-20261114` de `Conquereleven/tres-leches-demo`, en **una rama remota no-`main`** y **un Draft PR**; luego obtener CI del SHA remoto. Esta es una publicación de código, no la liberación a Production.

**Verificaciones ya disponibles:** Hermes reportó worktree limpio, ancestry, permisos y revisión independiente PASS de Claude en el SHA exacto. GitHub remoto `main` sigue en `13c4609`; nueve workflows en `main` se inspeccionaron sin comando de deployment, y `commerce-ci.yml` hace push únicamente en `main`. Railway Production fue consultado en modo lectura: origen `main`, SHA `13c4609`, `live`, sin staged. La configuración de PR previews **no es visible** en la consulta realizada. No afirmar que esa política fue verificada.

**Decisión proporcional propuesta:** el agente ejecutor puede concluir el preflight de seguridad para **push de rama** con estas pruebas y corroboración local pertinente. Si pasa, realizar push **sin force** y verificar que Railway Production conserve el mismo SHA. Para **crear el Draft PR**, verificar antes el riesgo separado de preview environment; si no puede determinarse, detener **sólo ese efecto**, conservar la rama remota y comunicar una única brecha específica. Esta división no autoriza nuevos entornos ni cambios de Railway.

**Permisos:** GO existente para push no forzado + un Draft PR. NO GO para merge, deploy, crear infraestructura/preview manual, variables, secretos, datos o mensajes. Una integración a `main` podría disparar desplegado y siempre conserva su GO específico. El objetivo comercial es un Release Train final único, no un deploy por cada PR.

## 6. Evaluación de la propuesta y pruebas negativas

| Prueba de aceptación | Resultado exigido |
|---|---|
| A un agente se le vuelve a pedir el GO de push ya vigente. | Detecta el GO existente y continúa dentro del alcance; cero preguntas repetidas. |
| El push de feature branch es seguro, pero el PR preview es UNKNOWN. | Avanza el push si su prueba es suficiente; mantiene HOLD sólo para el PR que pudiera crear recursos. |
| Falta revisión independiente exigida por la política local. | No inventa PASS; solicita review real del SHA exacto. |
| Se intenta introducir un deploy a `main` bajo el GO de PR. | Bloquea; requiere GO de Production separado. |
| Archivo de descarga no existe o no es legible. | No genera enlace ni afirma entrega. |
| Un proveedor muestra «No change» tras selección. | No afirma configuración restaurada. |
| El asistente tiene conector de lectura, pero la acción específica lo prohíbe. | Respeta la exclusión; no confunde política general con permiso específico. |
| Se modifica el SHA o las pruebas dejan de aplicar. | Invalida sólo evidencia afectada y ejecuta verificaciones proporcionales. |

**Métricas piloto propuestas, sin inventar baseline:** intervenciones del Founder por tarea, GO duplicados, handoffs redundantes, tiempo hasta primer resultado ejecutable, tiempo hasta VERIFIED, enlaces inexistentes, acciones fuera de GO, defectos escapados a CI/UAT. Durante dos semanas medir baseline y comparar con el siguiente período comparable; sin prometer mejoras porcentuales no medidas. **Tolerancia cero**: operaciones no autorizadas, falsa verificación de Production y enlaces ficticios.

## 7. Adopción propuesta y límites

1. **COMPLETADO 2026-11-16:** Founder aprobó el contenido del RFC. La preparación y aprobación conceptual no equivalen a adopción técnica ni publicación.
2. Si se autoriza actualización del repositorio corporativo, Codex/Claude aplicarán el **mínimo delta** al estándar elegido, con revisión independiente proporcional y sin cambiar protecciones de release. No abrir un PR ni fusionar cambios hasta su GO específico.
3. Después, cada repositorio cliente adopta los cambios mediante su procedimiento propio. Los Draft PR #70/#77 de 3L no se dan por fusionados ni se reescriben sin reconciliación.
4. Confirmar carga de las instrucciones mediante sesión nueva y un test negativo de autorizaciones. Sólo entonces declarar la adopción técnica verificada.

## 8. Tarea única inmediata para Hermes: avanzar el GO existente

**Encargo ejecutable a pegar en Hermes, en la M2; no es una orden de Production.**

```text
HERMES | 3L P0/P1 | GO EXISTENTE | RESULTADO, NO HANDOFFS

Cliente/repo: 3L Pastelerías / Conquereleven/tres-leches-demo
DRI del código: Codex; Hermes coordina.
Rama local: local/payment-time-fulfillment-20261114
HEAD esperado: 06b94653e4cbe5e46fd4ef98bff5f45399ce1c85
GO válido: push NO forzado a rama no-main + un Draft PR hacia main.

Información de preflight ya cotejada por ChatGPT el 16-11-2026:
- GitHub main: 13c46096087a7e58caecb8e2625bc4fc34e73e7a.
- 9 workflows revisados: ninguno tiene deploy; push CI de commerce-ci sólo main.
- Railway Production, consulta read-only: repo 3L, rama main,
  SHA 13c4609, servicio live, sin staged changes.
- Entornos actuales visibles: production y paymennt-test.
- Política específica de PR previews: UNKNOWN. No la inventes.

A. Comprueba desde tu M2 identidad de repo, rama, HEAD, árbol limpio,
   upstream, permisos y que ninguna acción de la rama no-main toque Production.
   Reutiliza el PASS de Claude del SHA exacto y los tests existentes.
B. Si el push de la rama está acreditado como seguro, EJECUTA el push
   NO forzado a rama de revisión distinta de main. No cambies main.
   Verifica SHA remoto, y que Railway Production continúa en 13c4609.
C. Para crear el único Draft PR, verifica separadamente si PR previews
   pudieran crear recursos o desencadenar despliegues no autorizados.
   Si seguro y dentro del GO, crea Draft PR, no uno duplicado, y devuelve URL.
   Si ese efecto sigue incierto, conserva el push válido y deja HOLD SÓLO
   para Draft PR con la única evidencia adicional indispensable.
D. Devuelve sólo URL/estado de rama y PR, SHA, CI, Production sin cambios,
   revisión exacta y un recibo de cinco líneas en el handoff EXISTENTE.

PROHIBIDO: force-push, merge, deploy, Railway writes, PR previews manuales,
infraestructura, variables, credenciales, datos reales, pagos, clientes,
notificaciones, ampliación del scope o repetir suite 908 sin delta.
Si A demuestra un disparador real de Production, NO HAGAS push; muestra
el campo/trigger preciso y la mínima alternativa segura.
```

## 9. Disposición de este documento

**Estado:** FOUNDER APPROVED (contenido), **no integrado ni adoptado técnicamente en el repositorio corporativo**.  
**Ejecución 3L:** el GO de GitHub sigue vigente, pero el agente local todavía debe realizar el push/PR y aportar evidencia remota. Este RFC **no** certifica que ese trabajo ya se ejecutó.  
**Siguiente decisión empresarial:** revisar/aceptar o ajustar la enmienda; no se solicita ninguna aprobación adicional para el alcance de push + Draft PR existente.
