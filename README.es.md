# Open Skills · Biblioteca de habilidades para agentes de IA

[简体中文](README.md) · [繁體中文](README.zh-Hant.md) · [English](README.en.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md)

Una colección pública de Agent Skills prácticos. El chino simplificado es el idioma principal; también hay guías en chino tradicional, inglés, francés, alemán y español. Instala solo los Skills que necesites.

## Catálogo

| Categoría | Skill | Utilidad | Descarga |
| --- | --- | --- | --- |
| Herramientas e interoperabilidad de agentes | [Agent Tool Discovery](skills/agent-tool-discovery/README.es.md) | Encontrar y reparar el acceso a Skills, servidores MCP y herramientas CLI que funcionan en un agente local pero no aparecen en otro, conservando la configuración existente. | [ZIP](https://github.com/xisheng687/open-skills/releases/download/agent-tool-discovery-v1.0.2/agent-tool-discovery.zip) |

**1 Skill publicado.** Incluye instrucciones, referencias, prompts completos en chino e inglés y guías en seis idiomas. No contiene Skills privados ni datos del ordenador del mantenedor.

## Descargar y utilizar

1. Descarga el ZIP de un Skill o extrae del repositorio la carpeta completa `skills/<nombre>/`.
2. Conserva todos los archivos, referencias y la licencia. El ZIP del repositorio completo no es un paquete de importación de un solo Skill.
3. Sigue la [guía en español](skills/agent-tool-discovery/README.es.md) o copia el [prompt en inglés](skills/agent-tool-discovery/references/client-prompt.en.md) o [chino](skills/agent-tool-discovery/references/client-prompt.zh-CN.md). Puedes pedir al agente que responda en español.

Las rutas de instalación y las formas de invocación dependen del cliente y la versión. Un agente en la nube puede no tener acceso a los archivos locales. Descargar o instalar no autoriza automáticamente a ejecutar el procedimiento.

## Añadir más Skills

Cada Skill mantiene una carpeta estable `skills/<nombre>/`, con categoría y etiquetas en sus metadatos. Añade una guía principal en chino, una versión inglesa y las traducciones necesarias, y registra el Skill en el catálogo. Consulta las [normas de contribución](CONTRIBUTING.md), disponibles en chino e inglés.

## Privacidad y verificación

Solo se publican instrucciones genéricas y fuentes públicas: nunca credenciales, inventarios reales, rutas personales, servicios privados, copias de seguridad ni datos de clientes. La validación estática y del paquete no demuestra que funcione en todos los agentes.

[Licencia MIT](LICENSE), también incluida en cada paquete independiente.
