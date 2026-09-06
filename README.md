# Beauty Time — Automatización de Atención al Cliente

Sistema automatizado de procesamiento y clasificación de correos de atención al cliente mediante una arquitectura de 11 módulos en Make, integrando Google Gemini 1.5 Flash para inferencia y Airtable como base de datos relacional.

---

## 🔗 Enlaces Obligatorios de Entrega

* **Base de Datos Airtable (Modo Lectura):** [(https://airtable.com/invite/l?inviteId=invFrE0fj1mv4GABt&inviteToken=50e7e4c8eab1d1ecf737b4841238a86dd01d67fc47d91b6f6a07e653d56cbb0f&utm_medium=email&utm_source=product_team&utm_content=transactional-alerts)]
* **Diagrama de Arquitectura (PDF):** [Descargar PDF](./arquitectura.pdf)
* **Blueprint del Escenario (Make):** [Descargar JSON](./BeautyAgent IA - Flujo Gmail y Airtable.blueprint.json)

---

## 📐 Arquitectura de Contrato Unificado (JSON Draft-07)

El flujo interno de datos sigue el estándar estricto de transferencia expuesto en el Manual Operativo:

```json
{
  "ingestion": { "message_id": "string", "sender_email": "email" },
  "security": { "anonymized_hash": "SHA-256" },
  "ai_inference": { "intent": "solicitar_turno | informacion_servicios | reclamos" },
  "execution_route": { "applied_route": "string", "approved_by_human": "boolean" }
}
