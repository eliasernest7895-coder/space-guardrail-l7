# Space Guardrail L7 🛡️🚀

> Middleware proxy determinista de grado industrial en FastAPI para la auditoría, control y blindaje de LLMs y Agentes en producción.

## 🎯 El Problema
Desplegar LLMs y agentes autónomos directamente a producción expone a los sistemas a fallos críticos:
* **Goal Drift:** Saturación de contexto que hace olvidar las reglas de negocio iniciales.
* **Alucinaciones de Código:** Generación de bucles ineficientes O(N^2) o sintaxis rota.
* **Contaminación de Estados:** Mezcla de variables y falta de aislamiento entre subtareas.

## ⚡ La Solución: Arquitectura de 10 Pilares
Space Guardrail actúa como una aduana L7 inquebrantable que intercepta, audita, corrige y re-inyecta las peticiones al vuelo mediante lógica local en RAM, sin dependencias de cajas negras corporativas costosas.

### Componentes Clave del Motor:
1. **Compresión de Estado (Pilar 1):** Gestión optimizada de historiales largos.
2. **Verificación Causal / DAG (Pilar 2):** Control estricto de dependencias entre tareas.
3. **Poda Temprana (Pilar 3):** Filtrado preventivo de patrones de comandos basura.
4. **Aduana de Verdad Dura (Pilar 4):** Grounding estricto contra alucinaciones.
5. **Memoria Episódica (Pilar 5):** Caché local de soluciones exitosas en RAM.
6. **Planificación en Reversa (Pilar 6):** Backward chaining para descomposición atómica.
7. **Auditoría AST (Pilar 7):** Análisis sintáctico en caliente para garantizar complejidad lineal O(N).
8. **Scopes Jerárquicos Aislados (Pilar 8):** Cajas negras para evitar contaminación de variables.
9. **Portapapeles de Anclaje (Pilar 9):** Inyección de Pinned Prompts fijos para evitar el Goal Drift.
10. **Rebote Automático (Pilar 10):** Corrección interna autónoma ante fallos de auditoría.

---

## 🛠️ Stack Tecnológico
* **Core:** Python 3.10+ / FastAPI
* **Validación:** Pydantic v2
* **Concurrencia:** HTTPX (Async Client)
* **Auditoría:** Módulo nativo `ast` de Python

## 🚀 Despliegue Rápido
```bash
git clone [https://github.com/eliasernest7895-coder/space-guardrail-l7.git](https://github.com/eliasernest7895-coder/space-guardrail-l7.git)
cd space-guardrail-l7
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
