# Agent Tool Discovery · Detección y reparación de herramientas

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

**Categoría:** herramientas e interoperabilidad de agentes · **Versión:** 1.0.2

## Qué problema resuelve

« Ya lo instalé, pero otro agente no lo encuentra ». Los directorios de Skills, las configuraciones MCP y las sesiones de autenticación pueden variar. Una herramienta CLI funciona en la terminal, pero quizá no esté en el PATH de una aplicación de escritorio.

Este Skill identifica los agentes locales y sus herramientas, reutiliza una fuente común de Skills y elige detección nativa, enlaces simbólicos individuales o copias con seguimiento según la compatibilidad real. Adapta las definiciones MCP por cliente, comprueba las rutas CLI, crea un índice local y distingue archivos presentes, detección y llamadas satisfactorias.

## Descargar e instalar

Descarga el [ZIP independiente](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip) o extrae la carpeta completa `skills/agent-tool-discovery/`. Conserva todos los archivos y referencias. Ni SKILL.md por sí solo ni el ZIP de todo el repositorio es el paquete de importación completo de este Skill.

Los clientes compatibles pueden usar `~/.agents/skills/agent-tool-discovery/`; Claude Code usa `~/.claude/skills/agent-tool-discovery/`. Confirma el producto y la versión. Compara los paquetes existentes con el mismo nombre antes de sobrescribir nada.

Adjunta el ZIP o indica su carpeta extraída y pide:

> Instala solo este Skill en el directorio de Skills de usuario confirmado para este cliente. Conserva todo el paquete y las versiones en conflicto. Verifica su detección en una sesión nueva. No ejecutes todavía la auditoría ni la reparación.

## Utilizar

> Usa agent-tool-discovery para revisar los agentes y las herramientas de este ordenador. Solo informa; no modifiques nada. Responde en español.

> Usa agent-tool-discovery para revisar y reparar la detección de herramientas entre mis agentes locales. Conserva las configuraciones existentes. Pídeme ayuda si hace falta iniciar sesión o resolver un conflicto. Responde en español.

En Codex puedes invocar `$agent-tool-discovery`. Sin instalarlo, copia el [prompt completo en inglés](references/client-prompt.en.md) o [chino](references/client-prompt.zh-CN.md). Por defecto autorizan reparaciones reversibles limitadas; para una revisión sin cambios, indica « solo auditar, no modificar ».

## Autorización, privacidad y límites

Conserva las configuraciones, los estados desactivados y los ámbitos de proyecto. No instala dependencias, actualiza herramientas ni elimina originales; no copia credenciales OAuth ni secretos integrados a otros clientes. En modo de auditoría no crea índices, reglas, copias de seguridad ni tareas. Descargar o instalar no autoriza a reparar.

Los inventarios, copias de seguridad e informes permanecen en una ubicación local privada, fuera de repositorios versionados o compartidos públicamente. Es un Skill basado en instrucciones, sin servicio permanente ni script de subida, y necesita acceso local. El catálogo no certifica compatibilidad. Lo que no se pueda verificar se señala como no verificado. Los productos de terceros tienen sus propias políticas de datos.

## Comprobaciones periódicas opcionales

Al terminar puedes elegir comprobaciones periódicas. Deben confirmarse el consentimiento, la frecuencia, el programador y el acceso local. Por defecto son de solo lectura y no notifican cuando nada cambia. La reparación automática requiere otra autorización; no inicia sesión ni resuelve conflictos automáticamente.

[Licencia MIT](LICENSE).
