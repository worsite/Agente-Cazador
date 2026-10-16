---
name: accion
description: Modo acción. Al invocar /accion se activan juntas las skills de ingeniería de superpowers (brainstorming, planes, TDD, debugging, revisión, verificación, git worktrees…), la guía de frontend system design y la guía de Fabric.js. Úsala cuando el usuario escriba /accion o pida pasar de la idea/brief a construir, depurar o entregar software con proceso disciplinado.
---

# /accion — pasar a la ejecución

Al invocarse, esta skill **carga y aplica juntos** tres paquetes que viven en esta carpeta. Los `SKILL.md` anidados NO están registrados como skills independientes: léelos con Read desde la ruta indicada cuando toque.

Base: `.claude/skills/accion/`

> Referencias cruzadas: dentro de los archivos de superpowers, `superpowers:<nombre>` significa **leer `superpowers/<nombre>/SKILL.md`** (no hay herramienta Skill para ellas).
> Excepción: las instrucciones del usuario y `CLAUDE.md` tienen prioridad sobre estas skills.

## Paso 0 — Al activarse
1. Lee `superpowers/using-superpowers/SKILL.md` (cómo usar el conjunto: si una skill puede aplicar, se consulta antes de responder).
2. Identifica la tarea del usuario (si viene de un BRIEF MAESTRO de `/cazador`, úsalo como especificación) y, si es interfaz, combina con `/diseno`.
3. Decide qué fase(s) del cuadro aplican y lee solo esos archivos.

## Cuadro de skills

### Proceso (superpowers/…)
| Situación | Leer |
|---|---|
| Construir algo nuevo / idea aún sin diseño | `brainstorming/SKILL.md` |
| Ya hay diseño aprobado, falta plan | `writing-plans/SKILL.md` |
| Ejecutar un plan escrito (en esta sesión) | `executing-plans/SKILL.md` |
| Plan con tareas independientes y subagentes | `subagent-driven-development/SKILL.md` |
| 2+ tareas independientes en paralelo | `dispatching-parallel-agents/SKILL.md` |
| Cualquier feature o bugfix antes de escribir código | `test-driven-development/SKILL.md` |
| Bug, test fallido o comportamiento inesperado | `systematic-debugging/SKILL.md` |
| Trabajo aislado en una rama/worktree | `using-git-worktrees/SKILL.md` |
| Pedir revisión de lo hecho | `requesting-code-review/SKILL.md` |
| Recibir comentarios de revisión | `receiving-code-review/SKILL.md` |
| Antes de decir "listo/arreglado/pasa" | `verification-before-completion/SKILL.md` |
| Terminar la rama (merge/PR/limpieza) | `finishing-a-development-branch/SKILL.md` |
| Crear o editar skills | `writing-skills/SKILL.md` |
| Diagnosticar fallos de estas skills | `diagnosing-superpowers/SKILL.md` |

Orden típico: brainstorming → using-git-worktrees → writing-plans → (executing-plans | subagent-driven-development) con test-driven-development → requesting-code-review → verification-before-completion → finishing-a-development-branch.

### Arquitectura frontend (`frontend-system-design/`)
Lee `frontend-system-design/README.md` (checklist de Engineering, High Level y Low Level Design: SPA/MPA, SSR/SSG/CSR, stack, SEO, CI/CD, rendimiento, seguridad, etc.) al **decidir arquitectura** de una app web y úsalo como lista de verificación. El PDF `FE_SE_Handbook.pdf` es la versión completa; léelo (con `pages`) solo si hace falta profundidad. La guía es agnóstica de framework.

### Canvas / editores gráficos (`fabricjs/`)
Si la tarea implica canvas HTML5 (editores, mockups, firmas, imágenes interactivas), lee `fabricjs/GUIA.md`. `fabricjs/fabricjs-open-pr/` solo aplica para contribuir al repo fabric.js.

## Reglas
- No inventes pasos: sigue el archivo leído. Si dos skills chocan, prefiere la del proceso más estricto salvo que el usuario diga otra cosa.
- Para un MVP de `/cazador`: mantén el alcance del brief; no añadas funciones excluidas.
- No des por terminado sin ejecutar la verificación real (`verification-before-completion`).
- Licencias: MIT de cada proyecto incluidas (`superpowers/LICENSE`, `frontend-system-design/LICENSE`, `fabricjs/LICENSE`).
