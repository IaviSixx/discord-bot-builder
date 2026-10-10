# Discord Bot Builder

Programa de escritorio para crear bots de Discord por módulos: identidad, módulos configurables con vista previa, generación de un proyecto discord.js, hosting en Railway e historial de versiones.

Este repositorio publica los **instaladores** y las **actualizaciones automáticas** del programa. El código fuente no está aquí.

## Instalar

1. Descarga `Discord-Bot-Builder-Setup-x.y.z.exe` de la última versión en [Releases](../../releases/latest).
2. Windows puede mostrar "Windows protegió su PC" porque el instalador no está firmado: **Más información → Ejecutar de todas formas**.
3. Para instalar y arrancar bots desde el programa hace falta Node.js 18.17 o superior.

Desde la 0.5.0, el programa busca versiones nuevas aquí, las descarga solo y ofrece **Reiniciar y actualizar**.

## Publicar una versión

Cada versión es una *release* con la etiqueta `vX.Y.Z` y tres archivos generados por `npm run dist:win`:

- `Discord-Bot-Builder-Setup-X.Y.Z.exe`
- `Discord-Bot-Builder-Setup-X.Y.Z.exe.blockmap`
- `latest.yml`

Los programas instalados leen `latest.yml` de la última release para saber si hay versión nueva.
