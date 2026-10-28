# DockSpark

[English](README.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Español](README.es.md)

DockSpark te permite cambiar de perfil de navegador directamente desde el Dock de macOS. Coloca el puntero sobre el icono de un navegador compatible y elige el perfil que quieras sin abrir el menú de perfiles del navegador.

[Descargar la última versión](https://github.com/DockSpark/DockSpark/releases/latest)
· [Sitio web](https://dockspark.app)
· [Historial de cambios (en inglés)](CHANGELOG.md)
· [Informar de un problema](https://github.com/DockSpark/DockSpark/issues)

## Funciones

- Cambia de perfil desde un panel emergente junto al icono del navegador en el Dock
- Gestiona los perfiles de navegador desde una app nativa de macOS
- Personaliza los nombres y colores para identificar los perfiles rápidamente
- Elige qué perfiles con nombre aparecen en el menú al pasar el puntero sobre el Dock
- Usa DockSpark Free o desbloquea un número ilimitado de navegadores y perfiles con Pro
- Muestra u oculta los iconos de la barra de menús y del Dock
- Busca actualizaciones desde la app
- Abre la documentación o envía comentarios estructurados desde el menú Ayuda
- Usa la app en inglés, chino simplificado, chino tradicional, japonés, coreano, alemán, francés o español
- Ajusta el tamaño de los paneles al de los iconos del Dock, incluido el efecto de ampliación
- Desactiva el análisis anónimo de uso en los ajustes generales

## Requisitos

- macOS 14.0 o posterior
- Mac con chip de Apple o procesador Intel
- Un navegador compatible que se mantenga en el Dock

### Navegadores compatibles

| Navegador | Cambio de perfil desde el Dock |
| --- | --- |
| Safari | Compatible |
| Firefox | Compatible |
| Google Chrome | Compatible |
| Chromium | Compatible |
| Microsoft Edge | Compatible |
| Brave Browser | Compatible |
| Vivaldi | Compatible |
| Opera | Compatible |
| Opera GX | Compatible |
| Arc | Compatible |

Safari, Google Chrome y Firefox se activan de forma predeterminada si están instalados. El plan Free permite un navegador activado y tres perfiles con nombre por navegador. Las entradas de navegación privada y modo incógnito no cuentan para el límite de perfiles. Pro elimina estos límites. Puedes añadir otros navegadores instalados desde la lista de aplicaciones.

## Instalación

### Homebrew

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

### Descarga manual

1. Abre la [última versión](https://github.com/DockSpark/DockSpark/releases/latest).
2. Descarga `DockSpark-0.5.0.dmg`. No descargues los archivos de código fuente que GitHub genera automáticamente.
3. Abre la imagen de disco y arrastra `DockSpark.app` a la carpeta Aplicaciones.
4. Inicia DockSpark y concede los permisos de macOS solicitados.

El archivo `DockSpark-0.5.0.zip` también está disponible para la instalación manual.

DockSpark está firmado con un certificado Developer ID y notarizado por Apple.

## Permisos

DockSpark solo solicita los permisos del sistema necesarios para cambiar de perfil:

- **Accesibilidad** detecta la interacción del puntero con los iconos de navegadores compatibles en el Dock.
- **Automatización** permite que DockSpark solicite al navegador seleccionado que cambie de perfil.
- **Acceso total al disco** es opcional. DockSpark lo usa únicamente para descubrir los metadatos de los perfiles de Chromium y Firefox.

Puedes revisar o revocar estos permisos en cualquier momento en **Ajustes del Sistema > Privacidad y seguridad**.

## Uso

1. Añade un navegador compatible al Dock.
2. Configura el navegador y sus perfiles en DockSpark.
3. Coloca el puntero sobre el icono del navegador en el Dock.
4. Selecciona un perfil en el panel emergente.

## Skill para asistentes de IA

El [skill de DockSpark](skills/dockspark/SKILL.md) ayuda a los asistentes de IA a explicar qué hace DockSpark y cuándo resulta útil, guiar la instalación y el uso diario, encontrar documentación oficial y resolver problemas habituales. La versión **0.5.0** del skill sigue la versión de la app; las guías incluidas se han revisado para DockSpark 0.5.0. El asistente responde en tu idioma.

Instálalo con [Skills CLI](https://github.com/vercel-labs/skills) (requiere Node.js; consulta su documentación para conocer los requisitos actuales):

```sh
npx skills add DockSpark/DockSpark --skill dockspark
```

Elige tu asistente de IA cuando se te solicite. De forma predeterminada, la instalación se aplica al proyecto actual; añade `-g` para una instalación global. El comando de GitHub requiere que el skill esté publicado en este repositorio. Desde una copia local, usa:

```sh
npx skills add . --skill dockspark
```

Para la [instalación manual en Codex](https://developers.openai.com/codex/skills/), copia todo el directorio `skills/dockspark`, incluidos `references/` y `agents/`, a `~/.agents/skills/dockspark` o a `.agents/skills/dockspark` dentro de tu proyecto. Otros asistentes pueden usar directorios de skills diferentes. Vuelve a cargar los skills de tu asistente o inicia una nueva sesión si el skill no aparece.

Ejemplos de consultas:

- `Usa $dockspark para explicarme en qué me puede ayudar DockSpark.`
- `Usa $dockspark para ayudarme a configurar perfiles de Chrome.`
- `Usa $dockspark para averiguar por qué no pasa nada al colocar el puntero sobre un icono del Dock.`

Puedes hacer las mismas preguntas en inglés o en otro idioma. El skill ofrece orientación; instala DockSpark por separado para usar la app. Con cada nueva versión de la app, revisa las guías y los enlaces oficiales del skill y actualiza conjuntamente su versión y la versión de referencia revisada.

## Captura de pantalla

![Ventana de gestión de perfiles de DockSpark](Assets/img_dockspark.jpg)

> La captura muestra la interfaz de DockSpark. La versión 0.5.0 permite cambiar de perfil desde el Dock en Safari, Firefox, Chrome y los demás navegadores basados en Chromium de la tabla anterior.

## Actualizaciones

DockSpark utiliza Sparkle para las actualizaciones dentro de la app. También puedes descargar versiones manualmente desde la [página de lanzamientos](https://github.com/DockSpark/DockSpark/releases).

## Integridad de los archivos publicados

Las sumas de comprobación SHA-256 son:

```text
DockSpark-0.5.0.dmg  90c0f9369d67eb33e6939b1cac008ec70277f7c176c0f2a1aa0e50fb08e85eff
DockSpark-0.5.0.zip  1d7eb10b9ce7736f2a1e5f1fd790eebb399675fadb95702a6032f329f65db129
```

Compruébalas después de la descarga:

```sh
shasum -a 256 DockSpark-0.5.0.dmg DockSpark-0.5.0.zip
```

## Comentarios

Usa [GitHub Issues](https://github.com/DockSpark/DockSpark/issues) para informar de errores o sugerir mejoras. Al informar de un error, incluye la versión de macOS, la versión del navegador y los pasos para reproducir el problema.

Este repositorio contiene los materiales públicos de distribución de DockSpark. No incluye el código fuente de la aplicación.
