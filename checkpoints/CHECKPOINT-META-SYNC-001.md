# CHECKPOINT-META-SYNC-001
**Checkpoint ID:** `CHECKPOINT-META-SYNC-001`  
**Fecha:** 20 de Septiembre de 2026  
**Repositorio:** `aliuntravelsrl-hash/-METAINTELIGENCIA-DOMAIN`  
**Alcance:** Formalización del Perímetro de Sincronización de Metainteligencia  
**Repository Sync Version:** `META-SYNC-001`  
**Intelligence Baseline:** `INTELLIGENCE-BASELINE-000` (`FOUNDATIONAL / BASELINE-PENDING`)  
**Estado:** ✅ CERTIFICADO / READ-ONLY BOUND  

---

## 1. Contexto y Decisión

Se materializó el contrato canónico `META-SYNC-MANIFEST-v1.md` estableciendo con exactitud:
- Qué artefactos pertenecen a Metaintelligence (`OWNED`).
- Qué artefactos son heredados de `atlas-cos-v1` (`INHERITED`).
- Qué artefactos son referenciados desde `atlas-curator-office` y repositorios de producto (`REFERENCED`).
- Qué artefactos quedan expresamente fuera del dominio (`EXCLUDED`).

---

## 2. Invariante de Continuidad

$$\text{Repository Sync Version (META-SYNC-001)} \neq \text{Intelligence Baseline Version (INTELLIGENCE-BASELINE-000)}$$

Este checkpoint certifica la delimitación del repositorio sin avanzar la línea base de inteligencia.

---

## 3. Evidencia Verificada
- Manifiesto canónico: `META-SYNC-MANIFEST-v1.md`
- Distinción de versiones: `VERSION.md`
- Actualización mínima de contexto: `README.md`
