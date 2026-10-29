# Devkron 2.0: paquetes de distribución

Motor de Devkron (DKL) con su FastCGI, bibliotecas y herramientas (dklwebsvr, w3se, httptn e iis2dkl), listo para
descomprimir en una carpeta. Trae su propio .NET: no requiere instalar nada más. No incluye instalador ni licencia.

## Versión vigente: 2.0.0-rc.1

| Archivo | Plataforma | SHA-256 |
|---|---|---|
| [Devkron-2.0-Linux-x64.zip](2.0.0-rc.1/Devkron-2.0-Linux-x64.zip) | Linux x64 | `0a224bcf9d6922f834b3d344e53c4f2f828413a144cca4fa9f10dba82e531955` |
| [Devkron-2.0-Windows-x64.zip](2.0.0-rc.1/Devkron-2.0-Windows-x64.zip) | Windows x64 | `536a4a43ca8de53146c003e9276097f09ae6e75b94739855a5c464222b53de8a` |

Bibliotecas con código de terceros (opcionales, se descomprimen en la carpeta de `dkl`):
[csv](2.0.0-rc.1/thirdparty/dkl2-csv-1.0.0.zip), [office](2.0.0-rc.1/thirdparty/dkl2-office-1.0.0.zip),
[image](2.0.0-rc.1/thirdparty/dkl2-image-1.0.0.zip), [html](2.0.0-rc.1/thirdparty/dkl2-html-1.0.0.zip),
[markdown](2.0.0-rc.1/thirdparty/dkl2-markdown-1.0.0.zip). Sumas en [SHA256SUMS](2.0.0-rc.1/SHA256SUMS);
versiones y commits en [manifest.json](2.0.0-rc.1/manifest.json).

## Verificar y descomprimir

```
cd 2.0.0-rc.1 && sha256sum -c SHA256SUMS
unzip Devkron-2.0-Linux-x64.zip -d /opt          # Windows: Expand-Archive Devkron-2.0-Windows-x64.zip C:\
/opt/Devkron-2.0-Linux-x64/dkl -license          # sin licencia de 2.0 queda en modo demostración
```

## Documentación

- [Descargas y contenido de los paquetes](https://docs.induxsoft.net/es/devkron/2.0/instalacion/descargas)
- Instalación: [Linux](https://docs.induxsoft.net/es/devkron/2.0/instalacion/linux) ·
  [Windows](https://docs.induxsoft.net/es/devkron/2.0/instalacion/windows)
- [Licencia](https://docs.induxsoft.net/es/devkron/2.0/instalacion/licencia)
- [dklwebsvr](https://docs.induxsoft.net/es/devkron/2.0/instalacion/dklwebsvr) ·
  [IIS (iis2dkl)](https://docs.induxsoft.net/es/devkron/2.0/instalacion/iis) ·
  [w3se](https://docs.induxsoft.net/es/productos/tools/w3se/) ·
  [httptn](https://docs.induxsoft.net/es/productos/tools/httptn/)
- [Devkron](https://docs.induxsoft.net/es/devkron)

Cada versión vive en su propia carpeta y no se sobrescribe.
