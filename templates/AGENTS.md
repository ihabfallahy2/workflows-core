# AGENTS.md — flujo de trabajo de este repositorio

## Flujo obligatorio
Todo cambio sigue: Issue → rama (`feat/` o `fix/`) → PR contra `develop` → merge → release automático al mergear `develop` en `master`.

## Comandos
1. `npx @ihabfallahy2/agentic-wf start --type <fix|feat> --title "..."` — crea el issue y la rama.
2. Desarrollar y verificar.
3. `npx @ihabfallahy2/agentic-wf finish` — abre el PR contra `develop`.
4. `npx @ihabfallahy2/agentic-wf sync` — trae la última versión de este archivo y de los workflows, si han cambiado en `workflows-core`.

## Reglas
- Nunca commitear directo a `master` o `develop`.
- Mensajes de commit en formato conventional commits (`feat:`, `fix:`, `chore:`...) porque el versionado semántico y el changelog dependen de ellos.
- El release y el changelog son automáticos — no editar `CHANGELOG.md` a mano.
- Antes de empezar una tarea nueva, correr `wf sync` si ha pasado tiempo desde el último bootstrap.
