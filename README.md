# Devkron 2.0 LTS: paquetes de distribución

Motor de Devkron (DKL) con su FastCGI, bibliotecas y herramientas (dklwebsvr, w3se, httptn e iis2dkl), listo para
descomprimir en una carpeta y empezar a desarrollar.

## Versión vigente: 2.0.5.0

| Archivo | Plataforma | SHA-256 |
|---|---|---|
| [Devkron-2.0.5.0-Linux-x64.zip](2.0-LTS/2.0.5.0/Devkron-2.0.5.0-Linux-x64.zip) | Linux x64 | `5fb7f5e0456be24540363ed9f70ad76bfc86fb5b7c06dc19991e69964338c823` |
| [Devkron-2.0.5.0-Windows-x64.zip](2.0-LTS/2.0.5.0/Devkron-2.0.5.0-Windows-x64.zip) | Windows x64 | `3841489b13392b91580d77b71d5f6f89e2d62c451d8dd9a24b49b614c5a26428` |

Sumas en [SHA256SUMS](2.0-LTS/2.0.5.0/SHA256SUMS); versiones y commits de cada componente en [manifest.json](2.0-LTS/2.0.5.0/manifest.json).

Desde 2.0.5.0 la numeración tiene cuatro partes (V.x.y.z) y el nombre del zip la lleva; la carpeta que trae dentro sigue
siendo `Devkron-2.0-Linux-x64` (o `-Windows-x64`), como en las anteriores.

Novedades de 2.0.5.0: un `runscript`/`runcode` anidado ya no retiene lo que deja hasta el final del programa que lo
lanzó (un programa largo que lanza muchos trabajadores ya no crece en memoria con cada uno ni llega al tope del pool
de MySQL por conexiones que no se cerraron); `_import_library` acepta en Linux rutas escritas con `\` y rutas
relativas con carpeta; y una función .NET mapeada ya no se llama con `0` cuando falla una función de usuario en sus
argumentos: se va directo al `exception` ([novedades](https://docs.induxsoft.net/es/devkron/2.0/introduccion/novedades.md)).

> **No use 2.0.3.** Tiene la regresión de `ref x:y` que corrige 2.0.4; se conserva solo como registro.

Las versiones anteriores siguen en [2.0-LTS/2.0.4](2.0-LTS/2.0.4/), [2.0-LTS/2.0.3](2.0-LTS/2.0.3/) (no usar),
[2.0-LTS/2.0.2](2.0-LTS/2.0.2/) y [2.0-LTS/2.0.1](2.0-LTS/2.0.1/).

## Verificar y descomprimir

```
cd 2.0-LTS/2.0.5.0 && sha256sum -c SHA256SUMS
unzip Devkron-2.0.5.0-Linux-x64.zip -d /opt      # Windows: Expand-Archive Devkron-2.0.5.0-Windows-x64.zip C:\
/opt/Devkron-2.0-Linux-x64/dkl -license          # sin licencia de 2.0 queda en modo demostración
```

## Bibliotecas con código de terceros

Opcionales, con su propio ciclo de versiones; se descomprimen en la carpeta de `dkl`. Índice con la versión mínima
del motor de cada una en [2.0-LTS/thirdparty](2.0-LTS/thirdparty/README.md).

| Biblioteca | Versión vigente | Motor mínimo |
|---|---|---|
| [csv](2.0-LTS/thirdparty/dkl2-csv-1.0.0.zip) | 1.0.0 | 2.0.0 |
| [office](2.0-LTS/thirdparty/dkl2-office-1.0.0.zip) (xlsx, doc) | 1.0.0 | 2.0.0 |
| [image](2.0-LTS/thirdparty/dkl2-image-1.0.0.zip) | 1.0.0 | 2.0.0 |
| [html](2.0-LTS/thirdparty/dkl2-html-1.0.0.zip) | 1.0.0 | 2.0.0 |
| [markdown](2.0-LTS/thirdparty/dkl2-markdown-1.0.0.zip) | 1.0.0 | 2.0.0 |

## Devkron Edge (dkle)

Runtime ligero y gratuito de DKL para microservicios y conectores entre API HTTP (Linux x64, Linux ARM64 y Windows
x64), con su propio ciclo de versiones en [2.0-LTS/dkle](2.0-LTS/dkle/README.md). Versión vigente: **2.0.1**.
Documentación: https://docs.induxsoft.net/es/devkron/2.0/dkle/

## Herramientas de desarrollo

- **Depurador `dkl-debug`** (Linux x64, Linux ARM64, Windows x64), con su propio ciclo de versiones en
  [2.0-LTS/dkl-debug](2.0-LTS/dkl-debug/README.md). Versión vigente: **0.1.0** (motor 2.0.2).
- **Extensión para VS Code y Cursor** (`.vsix`), en [2.0-LTS/vscode](2.0-LTS/vscode/README.md). Versión vigente:
  **0.1.0**.

## Versiones

Cada línea LTS tiene su carpeta (`2.0-LTS/`) y cada distribución del motor su subcarpeta, que nunca se sobrescribe:
`2.0-LTS/2.0.1/` … `2.0-LTS/2.0.4/`, `2.0-LTS/2.0.5.0/`… (una línea futura sería `2.1-LTS/2.1.0.0/`). Hasta 2.0.4 los zips
conservan el nombre de la línea (`Devkron-2.0-<SO>-x64.zip`); desde 2.0.5.0 llevan la versión completa
(`Devkron-2.0.5.0-<SO>-x64.zip`). La versión vigente es la más alta de la línea. Las bibliotecas de terceros van
en `2.0-LTS/thirdparty/` con su propia versión en el nombre del zip, Devkron Edge en `2.0-LTS/dkle/<versión>/`, el depurador en `2.0-LTS/dkl-debug/<versión>/` y la extensión en `2.0-LTS/vscode/<versión>/`.

## Documentación

- [Descargas y contenido de los paquetes](https://docs.induxsoft.net/es/devkron/2.0/instalacion/descargas.md)
- Instalación: [Linux](https://docs.induxsoft.net/es/devkron/2.0/instalacion/linux.md) ·
  [Windows](https://docs.induxsoft.net/es/devkron/2.0/instalacion/windows.md)
- [Licencia](https://docs.induxsoft.net/es/devkron/2.0/instalacion/licencia.md)
- [Repositorios de conexiones en base de datos](https://docs.induxsoft.net/es/devkron/2.0/instalacion/repositorio-conexiones.md)
- [dklwebsvr](https://docs.induxsoft.net/es/devkron/2.0/instalacion/dklwebsvr.md) ·
  [IIS (iis2dkl)](https://docs.induxsoft.net/es/devkron/2.0/instalacion/iis.md) ·
  [w3se](https://docs.induxsoft.net/es/productos/tools/w3se/) ·
  [httptn](https://docs.induxsoft.net/es/productos/tools/httptn/)
- [Devkron Edge (dkle)](https://docs.induxsoft.net/es/devkron/2.0/dkle/)
- [Devkron](https://docs.induxsoft.net/es/devkron/)
