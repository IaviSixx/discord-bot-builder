# Discord Bot Builder

Programa de escritorio para crear bots de Discord por módulos: identidad, módulos configurables con vista previa, generación de un proyecto discord.js, hosting en Railway e historial de versiones.

Este repositorio publica los **instaladores** y las **actualizaciones automáticas** del programa. El código fuente no está aquí.

## Instalar en Windows

1. Descarga `Discord-Bot-Builder-Setup-x.y.z.exe` de la última versión en [Releases](../../releases/latest).
2. Windows puede mostrar "Windows protegió su PC" porque el instalador no está firmado: **Más información → Ejecutar de todas formas**.
3. Para instalar y arrancar bots desde el programa hace falta Node.js 18.17 o superior.

## Instalar en Mac (desde la 0.8.1)

Necesita macOS 13 Ventura o posterior.

1. Mira qué chip tiene tu Mac: menú  → **Acerca de este Mac**. Si pone *Apple M1, M2, M3…* descarga `Discord-Bot-Builder-x.y.z-mac-arm64.zip`; si pone *Intel*, `Discord-Bot-Builder-x.y.z-mac-x64.zip`.
2. Abre el .zip (se descomprime solo) y arrastra **Discord Bot Builder** a **Aplicaciones**. Si lo abres desde Descargas, el programa ofrece moverse él solo.
3. La primera vez macOS dirá que no puede comprobar la app, porque no está firmada con un certificado de Apple. Pulsa **Hecho**, ve a **Ajustes del Sistema → Privacidad y seguridad** y, abajo, pulsa **Abrir igualmente** junto a "Discord Bot Builder". Solo hace falta una vez.
   Si en vez de eso dice que la app **está dañada**, abre **Terminal** y escribe `xattr -cr "/Applications/Discord Bot Builder.app"` (quita la marca de "descargado de internet"); después ábrela normal.
4. Al guardar tokens, macOS puede preguntar si el programa puede usar el Llavero: **Permitir siempre**.
5. Para probar bots en el Mac hace falta Node.js (instalador de macOS en nodejs.org, o Homebrew).

Las versiones de Mac se actualizan solas igual que la de Windows; las descarga el propio programa, así que macOS no vuelve a pedir permiso.

## Actualizaciones

Desde la 0.5.0 (Windows) y la 0.8.1 (Mac), el programa busca versiones nuevas aquí, las descarga solo y ofrece **Reiniciar y actualizar**.

## Publicar una versión

Cada versión es una *release* con la etiqueta `vX.Y.Z` y estos archivos:

- Windows (`npm run dist:win`): `Discord-Bot-Builder-Setup-X.Y.Z.exe`, su `.blockmap` y `latest.yml`.
- Mac (`npm run dist:mac`): `Discord-Bot-Builder-X.Y.Z-mac-arm64.zip`, `Discord-Bot-Builder-X.Y.Z-mac-x64.zip` y `latest-mac.yml`.

Los programas instalados leen `latest.yml` (Windows) o `latest-mac.yml` (Mac) de la última release para saber si hay versión nueva. Los archivos se suben partidos en trozos por una rama `subir/vX.Y.Z` y el flujo *Publicar versión* los une, comprueba su SHA-512 y crea la release.
