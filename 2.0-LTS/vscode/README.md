# Extensión Devkron (DKL) para VS Code y Cursor

Soporte del lenguaje Devkron, o simplemente DKL, para Visual Studio Code, Cursor y VSCodium: resaltado de sintaxis
(DKL, modelos `.ddm` y plantillas `.htt`), fragmentos, autocompletado y ayuda de las funciones de la biblioteca,
diagnósticos al guardar, ejecutar el archivo actual y depurar con [dkl-debug](../dkl-debug/README.md).

## Versión vigente: 0.1.0

| Archivo | SHA-256 |
|---|---|
| [devkron-0.1.0.vsix](0.1.0/devkron-0.1.0.vsix) | `8dea9d5603e233b64ffa517d8d831e81260ac296cab41737c8a1b6a02d50a52c` |

Sumas en [SHA256SUMS](0.1.0/SHA256SUMS); versión y commit en [manifest.json](0.1.0/manifest.json).

## Instalar

- **VS Code / VSCodium:** Extensiones → «…» → *Install from VSIX…* y elegir `devkron-0.1.0.vsix`, o
  `code --install-extension devkron-0.1.0.vsix`.
- **Cursor:** igual, desde el panel de extensiones (*Install from VSIX*), o `cursor --install-extension devkron-0.1.0.vsix`.

## Ajustes principales

| Ajuste | Para qué |
|---|---|
| `devkron.dklPath` | Ruta de `dkl` para ejecutar y para los diagnósticos (si no hay `dkl-debug`) |
| `devkron.debuggerPath` | Ruta de `dkl-debug` para depurar y para diagnósticos con la línea real |

## Versiones

Cada versión va en su propia carpeta (`2.0-LTS/vscode/0.1.0/`…), que nunca se sobrescribe. La vigente es la más alta.
