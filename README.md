# Devkron 2.0 LTS: paquetes de distribución

Motor de Devkron (DKL) con su FastCGI, bibliotecas y herramientas (dklwebsvr, w3se, httptn e iis2dkl), listo para
descomprimir en una carpeta y empezar a desarrollar.

## Versión vigente: 2.0.2

| Archivo | Plataforma | SHA-256 |
|---|---|---|
| [Devkron-2.0-Linux-x64.zip](2.0-LTS/2.0.2/Devkron-2.0-Linux-x64.zip) | Linux x64 | `c5cbaf7ed89cb1a004ccecdaee12c2f008ae53e6cfa637a8083684591029f117` |
| [Devkron-2.0-Windows-x64.zip](2.0-LTS/2.0.2/Devkron-2.0-Windows-x64.zip) | Windows x64 | `1c223250f8144234ed09361635dba1381a9443bbcb3a263011f4a3d9e7e93663` |

Sumas en [SHA256SUMS](2.0-LTS/2.0.2/SHA256SUMS); versiones y commits de cada componente en [manifest.json](2.0-LTS/2.0.2/manifest.json).

Novedades de 2.0.2: repositorios de conexiones en base de datos seguros con varios hilos (con `SQLDic/` y la
herramienta `tools/dbrepo`), `connections.xml` se vuelve a leer si una conexión local falla y el archivo cambió,
pila de excepciones atrapadas con tope de 100 y dklwebsvr 1.1.0 ([novedades](https://docs.induxsoft.net/es/devkron/2.0/introduccion/novedades.md)).
La versión anterior sigue en [2.0-LTS/2.0.1](2.0-LTS/2.0.1/).

## Verificar y descomprimir

```
cd 2.0-LTS/2.0.2 && sha256sum -c SHA256SUMS
unzip Devkron-2.0-Linux-x64.zip -d /opt          # Windows: Expand-Archive Devkron-2.0-Windows-x64.zip C:\
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

## Versiones

Cada línea LTS tiene su carpeta (`2.0-LTS/`) y cada distribución del motor su subcarpeta, que nunca se sobrescribe:
`2.0-LTS/2.0.1/`, `2.0-LTS/2.0.2/`… (una línea futura sería `2.1-LTS/2.1.1/`). Los zips conservan el nombre de la
línea (`Devkron-2.0-<SO>-x64.zip`). La versión vigente es la más alta de la línea. Las bibliotecas de terceros van
en `2.0-LTS/thirdparty/` con su propia versión en el nombre del zip, y Devkron Edge en `2.0-LTS/dkle/<versión>/`.

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
