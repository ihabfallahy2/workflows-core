# workflows-core

Fuente de verdad del flujo estándar de issue → rama → PR → release para todos los proyectos.

Los proyectos consumidores no copian la lógica: referencian estos workflows vía `workflow_call`,
anclados a un tag (`@v1`). Cambiar algo aquí y taguear una nueva versión lo propaga a todos
los repos que usan `@v1`.

Bootstrap de un repo nuevo: `npx @ihabfallahy2/agentic-wf init`
Actualizar un repo existente: `npx @ihabfallahy2/agentic-wf sync`
