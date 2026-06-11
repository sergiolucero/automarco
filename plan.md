# Plan de Trabajo 90 Días · Automarco IA Acceleration

## 1. Objetivo General
Transformar automarco.cl en un canal inteligente capaz de predecir demanda, optimizar inventario, dinamizar pricing y automatizar la atención comercial, con foco en reducción de stock inmovilizado (‑18%), aumento de conversión digital (+10%) y productividad comercial (+35% en SLAs).

---

## 2. Estructura de Workstreams y Equipo

| Workstream | Foco | Líder propuesto | Roles clave |
|------------|------|-----------------|-------------|
| **WS1 · Data Foundation** | Lakehouse, taxonomía SKU, paneles directivos | Data Lead Automarco | Data engineer, BI analyst, ERP SME |
| **WS2 · Search & Copilotos** | Búsqueda híbrida, asistente IA | Product Owner Digital | ML engineer, UX, Integrations dev, Conversational designer |
| **WS3 · Demand & Pricing** | Forecasting, pricing dinámico, simulador | Head Comercial/Compras | Data scientist, Pricing analyst, ERP integrator |
| **WS4 · Campañas & CRM** | Segmentación RFM, workflows, analítica | Marketing Automation Lead | CRM specialist, Data analyst, Copy/Content |
| **PMO & Governance** | Alineación holding, comité IA | PM Automarco + Consultoría | Sponsor C-Level, Jurídico (datos), Change manager |

---

## 3. Ruta Temporal Detallada

### Semana 1-2 · Discovery & Accesos
- Taller técnico 360° (datos, sistemas, KPIs, quick wins).
- Inventario de fuentes (ERP, catálogos OEM, portal, WhatsApp, CRM).
- Definir arquitectura cloud preferida, gobernanza datos, backlog priorizado.
- **Hitos:** accesos aprobados, plan de ingesta, modelo de datos de referencia draft.

### Semanas 2-4 · Data Foundation + Quick Wins Search
**Entregables clave:**
1. **Lakehouse v0**
   - Pipelines diarios ERP/portal → storage central (Delta/BigQuery/Snowflake).
   - Normalización taxonomía SKU y equivalencias cross-holding.
2. **Dashboard ejecutivo v0**
   - Métricas: rotación, fill-rate, aging, margen, stock crítico top 50.
3. **Prototype búsqueda inteligente**
   - Índice semántico + OEM + filtros; PoC foto → SKU (modelo pretrained + fine tuning).
4. **Backlog Copiloto**
   - Intenciones, fuentes de conocimiento, flujos de validación.

**Decisiones:** stack BI, política de accesos, priorización líneas críticas.

### Semanas 5-8 · Demand Forecasting & Pricing Experiments
**Entregables clave:**
1. **Modelo demanda multinivel (SKU/Bodega/Semana)**
   - Feature store: estacionalidad, lead times, devoluciones, parque vehicular.
   - Evaluación vs base lineal: MAPE, bias.
2. **Pricing dinámico + simulador**
   - Guardrails por segmento (taller, flota, retail).
   - Panel “qué pasa si”: impacto en margen y conversión.
3. **Segmentación RFM + afinidad**
   - Scoring clientes; campañas piloto (alertas mantención, cross-holding).
4. **Playbook abastecimiento**
   - Alertas transferencia bodegas, lotes sugeridos.

**Hitos:** aprobación reglas pricing, GO/NOGO piloto live; integración con ERP orden de compra.

### Semanas 9-12 · Copilotos & Automatización Comercial
**Entregables clave:**
1. **Asistente experto Web/WhatsApp (beta → prod)**
   - FAQs, compatibilidad, ETA despacho, upsell + bundles.
   - Conectado a disponibilidad real-time + pricing propuesto.
2. **Recomendador portal**
   - Bundles consumibles, sustitutos, “clientes similares compraron”.
3. **Orquestador campañas IA**
   - Workflows automáticos: recupero de carrito B2B, alertas stock crítico, cross-holding.
4. **Playbook gobernanza**
   - Comité quincenal IA, OKRs, modelo de mejora continua, política de datos.

---

## 4. Dependencias Técnicas

- Acceso APIs ERP, base de datos portal, catálogos OEM actualizados.
- Infraestructura cloud (cuenta, permisos, costos aprobados).
- Integración WhatsApp Business API / proveedor actual.
- Capacidad de lectura/escritura en backoffice de precios y stock.
- Legal & compliance: tratamiento datos clientes, términos asistente IA.

---

## 5. Gestión del Cambio & Acompañamiento

- Comunicación interna: boletín quincenal avances, training comercial asistente IA.
- Talleres específicos:
  - Compras: interpretación dashboard demanda.
  - Ventas: uso copiloto y campañas personalizadas.
  - Marketing: parametrización orquestador.
- Mesa gobierno datos (CIO, Comercial, Operaciones).

---

## 6. Riesgos & Mitigaciones

| Riesgo | Impacto | Mitigación |
|--------|---------|------------|
| Calidad/consistencia datos SKU | Alto | Cleansing automatizado + stewardship por unidad; reglas matching OEM. |
| Lead time implementaciones ERP | Medio | Plan paralelo con export batch mientras se liberan APIs. |
| Adopción Comercial Asistente | Medio | Co-diseño con ejecutivos, pilotos controlados, feedback loop semanal. |
| Sensibilidad precios | Alto | Guardrails, monitor en vivo, rollback plan. |
| Gestión cambio cross-holding | Medio | Comité IA interunidades, quick wins compartidos. |

---

## 7. KPIs de Éxito & Medición Continua

- **Inventario inmovilizado:** -18% (día 90).
- **Fill Rate:** 85% → 90% objetivo; alertas <85%.
- **Margen bruto protegido:** +6 pts vs baseline.
- **Conversión portal:** +10% vs mayo 2026.
- **SLA asistencia IA:** ≤30 s, ≥35% consultas automatizadas.
- **Elasticidad precio monitoreada:** panel activo con competidores principales.

Dashboards conectados a OKRs; cadencia semanal de revisión táctica + comité quincenal IA.

---

## 8. Próximos Pasos Inmediatos (Semana 0)

1. Confirmar equipo base y sponsors (nombres, disponibilidad).
2. Checklist accesos & seguridad (ERP, portal, repositorios).
3. Acordar stack cloud + presupuesto operativo.
4. Agendar workshop Discovery (90 min) + sesiones técnicas por workstream.
5. Configurar repositorio de proyecto, tablero de backlog, plantillas reportes.

> **Resultado esperado:** backlog priorizado y cronograma validados en la semana 1, con quick wins en marcha y ruta clara hacia despliegue integral en 90 días.
