# Euniprincez Digital v2026.1-MRP.pk 🛡️

### Sistema de Gestión de Seguridad (SGS), Auditoría y API Bridge

---

## 📝 Descripción del Proyecto
**[span_5](start_span)[span_6](start_span)[span_7](start_span)Euniprincez Digital** es un ecosistema de software propietario diseñado para la gestión automatizada, auditoría fiscal y protección criptográfica de infraestructura digital[span_5](end_span)[span_6](end_span)[span_7](end_span). [span_8](start_span)[span_9](start_span)[span_10](start_span)[span_11](start_span)El sistema integra un Panel de Control visual, un puente de comunicación de alta velocidad (API Bridge) conectado a SQL Server (SSMS), y un motor autónomo de respaldo en la nube y alertas en tiempo real[span_8](end_span)[span_9](end_span)[span_10](end_span)[span_11](end_span).

## 👤 Propiedad Intelectual y Autoría
* **[span_12](start_span)Titular y Desarrollador:** Juan Valentín García Espinoza[span_12](end_span)
* **[span_13](start_span)[span_14](start_span)ID Registro Legal:** GAEJ940310HSPRSN02[span_13](end_span)[span_14](end_span)
* **[span_15](start_span)[span_16](start_span)ID MEX:** 2608132112[span_15](end_span)[span_16](end_span)
* **[span_17](start_span)[span_18](start_span)Clave de Control Vital (Licencia):** `GAESJN94031024H400`[span_17](end_span)[span_18](end_span)

> ⚠️ **Aviso Legal:** Este software es propiedad intelectual privada. [span_19](start_span)[span_20](start_span)La alteración de los metadatos o el uso sin la clave de validación correspondiente constituye una violación legal a los derechos de autor[span_19](end_span)[span_20](end_span).

---

## 🛠️ Arquitectura del Sistema y Módulos

El ecosistema se divide en cuatro capas fundamentales:

1. **[span_21](start_span)[span_22](start_span)[span_23](start_span)SGS Panel de Control (Frontend Moderno):** Diseñado en Python (Streamlit) y maquetación web segura para la carga "Drag & Drop" de Certificados de Sello Digital (CSD del SAT) y monitoreo de transacciones[span_21](end_span)[span_22](end_span)[span_23](end_span).
2. **[span_24](start_span)[span_25](start_span)API Bridge (Backend):** Desarrollado con FastAPI y `pyodbc` para conectar la interfaz con SQL Server Management Studio mediante túneles seguros y tokens de alta entropía (64 caracteres)[span_24](end_span)[span_25](end_span).
3. **[span_26](start_span)[span_27](start_span)Euniprincez-Shield (Respaldos):** Script de automatización en Bash/Python que comprime y cifra en AES-256-CBC los archivos del SAT y logs, subiéndolos a Google Cloud Storage[span_26](end_span)[span_27](end_span).
4. **[span_28](start_span)Módulo de Notificaciones:** Integración nativa con la API de Telegram Bot para el envío de alertas móviles ante respaldos exitosos o bloqueos de seguridad[span_28](end_span).

---

## 🔒 Pilares de Seguridad Integrados

* **[span_29](start_span)[span_30](start_span)Ley de los Signos (Bloqueo Aritmético):** El motor valida estrictamente la precedencia y consistencia de las operaciones[span_29](end_span)[span_30](end_span). [span_31](start_span)[span_32](start_span)Si se intenta registrar un ingreso (`FF`) con un monto negativo, el sistema activa un bloqueo crítico e interrumpe la conexión con la base de datos[span_31](end_span)[span_32](end_span).
* **[span_33](start_span)[span_34](start_span)Validación de Entropía:** El API Bridge exige tokens de seguridad simétricos obligatorios de exactamente 64 caracteres para autorizar transacciones[span_33](end_span)[span_34](end_span).
* **[span_35](start_span)[span_36](start_span)[span_37](start_span)Aislamiento CSD:** Los archivos `.cer` y `.key` del SAT se procesan estrictamente en memoria o en el directorio seguro `/Euniprincez_Auth/` bajo permisos restrictivos (`chmod 600`)[span_35](end_span)[span_36](end_span)[span_37](end_span).

---

## 🚀 Requisitos e Instalación

### Dependencias de Python
Instala las librerías necesarias ejecutando:
```bash
pip install fastapi pyodbc streamlit cryptography requests python-dotenv
