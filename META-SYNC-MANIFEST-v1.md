# META-SYNC-MANIFEST-v1

## 1. Identity

```yaml
domain: METAINTELIGENCIA
repository: aliuntravelsrl-hash/-METAINTELIGENCIA-DOMAIN
contract: META-SYNC-MANIFEST-v1
author: ATLAS Curator Office / Antigravity
date: 2026-09-20
```

---

## 2. Repository Version

```text
REPOSITORY SYNC VERSION: META-SYNC-001
```

> **Definición de Versión de Repositorio:**  
> `META-SYNC-001` define el **primer perímetro formalizado de sincronización y correspondencia entre repositorios** para el dominio de Metainteligencia.  
> **NO constituye** ni representa una nueva *Intelligence Baseline*.

---

## 3. Intelligence Version

```text
INTELLIGENCE BASELINE: INTELLIGENCE-BASELINE-000
STATUS: FOUNDATIONAL / BASELINE-PENDING
```

### Invariante Fundamental de Versión
$$\text{Repository Sync Version (META-SYNC-001)} \neq \text{Intelligence Baseline Version (INTELLIGENCE-BASELINE-000)}$$

La versión de sincronización del repositorio gobierna la consistencia de los archivos, contratos y puentes entre repositorios Git.  
La *Intelligence Baseline* gobierna la madurez del conocimiento y la capacidad cognitiva demostrada del COS.

---

## 4. Owned Artifacts (Inventario Clasificado)

| Artifact | Path | Classification | Owner | Source of Truth | Sync Required | Notes |
|---|---|---|---|---|---|---|
| **Architecture Contract** | `ARCHITECTURE.md` | `OWNED` | Metaintelligence | Local (`-METAINTELIGENCIA-DOMAIN`) | Sí (Hacia Curator) | Cadena funcional TO-BE y control de inteligencia |
| **Genealogy Log** | `GENEALOGY.md` | `OWNED` | Metaintelligence | Local (`-METAINTELIGENCIA-DOMAIN`) | Sí (Hacia Curator) | Linaje evolutivo y Classifier como memoria de profundidad |
| **Intelligence Version** | `VERSION.md` | `OWNED` | Metaintelligence | Local (`-METAINTELIGENCIA-DOMAIN`) | No (Interno) | Definición inmutable de Baseline-000 |
| **Domain Manifesto** | `README.md` | `OWNED` | Metaintelligence | Local (`-METAINTELIGENCIA-DOMAIN`) | No (Interno) | Manifiesto y soberanía del dominio |
| **Sync Manifest** | `META-SYNC-MANIFEST-v1.md` | `OWNED` | Curator / Meta | Local (`-METAINTELIGENCIA-DOMAIN`) | Sí (Transversal) | Contrato canónico de sincronización inter-repo |
| **Drill Reports (001-025)**| `reports/DRILL-ACTIVE-*` | `OWNED` | Metaintelligence | Local (`-METAINTELIGENCIA-DOMAIN`) | No (Evidencia Local)| 24 reportes de investigación de identidad activa |
| **EVO Recommendation 026**| `reports/EVO-TO-BE-*` | `OWNED` | Metaintelligence | Local (`-METAINTELIGENCIA-DOMAIN`) | Sí (Hacia EVO/Curator)| Recomendación de selector de Active Capability |
| **Session Closures** | `checkpoints/SESSION-*` | `OWNED` | Metaintelligence | Local (`-METAINTELIGENCIA-DOMAIN`) | No (Local) | Cierres de sesión metodológicos |
| **Constitutional Laws** | `atlas-cos-v1/*` | `INHERITED` | Soberanía Directorial| `atlas-cos-v1` | Sí (Inbound) | Leyes fundamentales e Invariantes I-VI |
| **Swarm Orchestrator Profile**| `HERMES-SWARM-PROFILE` | `REFERENCED` | Curator Office | `atlas-curator-office` | Sí (Inbound) | Estándar de 21 Capítulos para Swarm |
| **Profile Resolution Standard**| `PROFILE-RESOLUTION-v1` | `REFERENCED` | Curator Office | `atlas-curator-office` | Sí (Inbound) | Metodología universal de resolución de perfiles |
| **Telemetry Bridges** | `ariadne-bridge / intel` | `REFERENCED` | Product / Curator | `atlas-hotels-v1` | Sí (Bidireccional) | Puentes telemétricos de salud y paridad |
| **Transactional DB Tables** | `public.crm_leads/bookings`| `EXCLUDED` | Business Domains | Supabase SSOT | No (Excluido) | Tablas operativas transaccionales |
| **Legal Corpus** | `aliun-legal-v1/*` | `EXCLUDED` | CLO / Hermes-QA | `aliun-legal-v1` | No (Excluido) | Términos y contratos legales |
| **Frontend Applications** | `atlas-booking / admin` | `EXCLUDED` | Frontend Teams | `-atlas-admin-v2`, etc. | No (Excluido) | Código de interfaz de usuario |

---

## 5. Source of Truth (Matriz de Autoridad)

| Elemento / Concepto | Canonical Source | Local Representation | Authority Level | Sync Direction |
|---|---|---|---|---|
| **Doctrina y Constitución COS** | `atlas-cos-v1` | `REFERENCE` | CANONICAL | Inbound (`atlas-cos-v1` ➔ Local) |
| **Estándares Metodológicos Curator** | `atlas-curator-office` | `REFERENCE` | CANONICAL | Inbound (`atlas-curator-office` ➔ Local) |
| **Investigaciones y Drills de Inteligencia** | `-METAINTELIGENCIA-DOMAIN` | `CANONICAL` | LOCAL | Outbound (Local ➔ Curator/Ecosistema) |
| **Catálogo de Capabilities** | Supabase (`capability_catalog`)| `PROJECTION` | CANONICAL (DB) | Inbound (DB ➔ Local) |
| **Telemetría de Integridad de Producto** | `atlas-hotels-v1` | `MIRROR / REFERENCE` | CANONICAL (Repo) | Bidireccional |
| **Eventos de Conocimiento (KBP)** | Supabase (`kbp_events`) | `PROJECTION` | CANONICAL (DB) | Inbound (DB ➔ Local) |

---

## 6. Cross-Repository Dependencies

| Dependency | Repository / System | Purpose | Direction | Canonical Source | Sync Required | Evidence |
|---|---|---|---|---|---|---|
| **Constitución COS** | `atlas-cos-v1` | Marco doctrinal y soberanía | Inbound | `atlas-cos-v1` | Sí | Citado en `README.md` y `ARCHITECTURE.md` |
| **Curator Framework** | `atlas-curator-office` | Drills, CCAMEL 360, Master Index | Inbound/Outbound| `atlas-curator-office` | Sí | Citado en `GENEALOGY.md` y `README.md` |
| **Mirror Kernel Telemetry**| `atlas-hotels-v1` | Integración telemétrica Ariadne/Intel| Bidireccional | `atlas-hotels-v1` | Sí | `ariadne-bridge.json` / `atlas-intel-bridge.json` |
| **Capability Registry** | Supabase DB | Mapeo de capacidades activas | Inbound | `public.capability_catalog` | Sí | Reporte `EVO-026` / `capability_resolver_map` |
| **Vector Memory Service** | OpenViking (`:1933`) | Memoria semántica vectorial | Bidireccional | VPS2 Container | Sí (Runtime) | `agent_persistent_memory` |
| **Hostinger / Mail Core** | `aliun-rrhh-v2` / n8n | Comunicación externa | N/A | `aliun-rrhh-v2` | No (Excluido) | Fuera del alcance de Metainteligencia |

---

## 7. Sync Boundary (Perímetro y Límites de Sincronización)

### What Sync Means (Qué SIGNIFICA Sincronización):
1. **Correspondencia de Contratos:** Asegurar que los contratos de interfaz telemétrica (`ariadne-bridge.json`, `atlas-intel-bridge.json`) sean idénticos entre Metainteligencia y los repositorios de producto.
2. **Consistencia de Referencias Doctrinales:** Validar que las citas a leyes, estándares y metodologías de `atlas-cos-v1` y `atlas-curator-office` apunten a versiones vigentes no revocadas.
3. **Visibilidad de Recomendaciones EVO:** Notificar formalmente al Curator de recomendaciones evolutivas generadas en `reports/EVO-*`.

### What Sync Does NOT Mean (Qué NO SIGNIFICA Sincronización):
1. **NO es Evolución Constitucional:** Sincronizar repositorios no altera la Constitución del COS.
2. **NO es Avance de Baseline:** `META-SYNC-001` no promueve `INTELLIGENCE-BASELINE-000` a `001`.
3. **NO es Adopción Automática:** Una recomendación en este dominio requiere autorización del Director General antes de materializarse.
4. **NO es Mutación de Base de Datos:** La sincronización no ejecuta DDL ni altera tablas en Supabase.
5. **NO es Creación de Arquitectura Paralela:** Queda prohibido inventar EventBuses o brokers alternativos.

---

## 8. Baseline Relationship (Relación con la Intelligence Baseline)

```text
META-SYNC-001 (Estado de Sincronización de Repositorio)
       │
       ├── Establece el perímetro de correspondencia documental y de contratos
       │
       └── NO AVANZA AUTOMÁTICAMENTE
               │
               ▼
      INTELLIGENCE-BASELINE-000 (Estado Actual: FOUNDATIONAL / BASELINE-PENDING)
```

### Secuencia Constitucional Obligatoria para Avanzar la Baseline:
Para que en el futuro la *Intelligence Baseline* avance a `INTELLIGENCE-BASELINE-001`, se requiere cumplir estrictamente la cadena de evidencia demostrada:

```text
INTELLIGENCE-BASELINE-000
         ↓
NUEVO CONOCIMIENTO GENERADO
         ↓
CLASIFICACIÓN FORMAL (Classifier)
         ↓
VERIFICACIÓN DE SUPERSESSION (No duplicidad)
         ↓
RECOMENDACIÓN EVO FORMAL
         ↓
AUTORIZACIÓN DIRECTORIAL SOBERANA (Director Aldo Hilario)
         ↓
MATERIALIZACIÓN VERIFICADA EN RUNTIME
         ↓
EVIDENCIA DE APRENDIZAJE DEMOSTRADO (LEARNING DEMONSTRATED)
         ↓
NUEVA BASELINE: INTELLIGENCE-BASELINE-001
```

---

## 9. Sync Validation (Procedimiento de Validación Reproducible)

Para comprobar el estado de sincronización entre `-METAINTELIGENCIA-DOMAIN` y los demás repositorios del COS, se aplica la siguiente matriz de verificación:

| Estado | Definición Operativa | Acción Requerida |
|---|---|---|
| **SYNCED** | El contrato, hash o referencia coincide exactamente con la fuente canónica. | Ninguna. Estado nominal. |
| **DRIFT** | La representación local difiere de la fuente canónica sin conflicto conceptual. | Actualizar representación local desde la fuente canónica. |
| **CONFLICT** | Modificaciones divergentes en ambas partes que colisionan en autoridad. | Escalar a Curator Office / Director para arbitraje. |
| **MISSING** | Un contrato o puente requerido no existe en el repositorio destino. | Materializar el artefacto faltante bajo este manifiesto. |
| **STALE** | La referencia apunta a una versión de doctrina o estándar deprecada. | Reemplazar referencia con la versión canónica vigente. |
| **UNVERIFIED** | Declarado documentalmente pero sin validación en commit o runtime. | Ejecutar drill o inspección física de comprobación. |

---

## 10. Genealogy (Linaje del Estado de Sincronización)

```text
ORIGIN (Creación del Repositorio -METAINTELIGENCIA-DOMAIN)
   ↓
DRILLS DE IDENTIDAD (001 a 025: Delimitación de Active Intelligence)
   ↓
EVO-026 (Recomendación TO-BE de Active Capability Selection)
   ↓
SESSION-CLOSURE-v1 (10 Sep 2026: Cierre del Drill de Identidad)
   ↓
META-SYNC-001 (20 Sep 2026: Establecimiento del Perímetro de Sincronización)
   ↓
[FUTUROS ESTADOS DE SINCRONIZACIÓN GOVERNADOS]
```

---

## 11. Checkpoint de Continuidad
Este manifiesto queda anclado al checkpoint de sincronización:  
[`checkpoints/CHECKPOINT-META-SYNC-001.md`](file:///C:/Users/Admin/Downloads/-METAINTELIGENCIA-DOMAIN/checkpoints/CHECKPOINT-META-SYNC-001.md).
