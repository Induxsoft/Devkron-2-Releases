# Devkron 2.0 LTS: paquetes de distribución

Motor de Devkron (DKL) con su FastCGI, bibliotecas y herramientas (dklwebsvr, w3se, httptn e iis2dkl), listo para
descomprimir en una carpeta. Trae su propio .NET: no requiere instalar nada más. No incluye instalador ni licencia.

## Versión vigente: 2.0.0

| Archivo | Plataforma | SHA-256 |
|---|---|---|
| [Devkron-2.0-Linux-x64.zip](2.0-LTS/2.0.0/Devkron-2.0-Linux-x64.zip) | Linux x64 | `e01a180c130cf2ba08616d9cbbe5727e241b4016c77640d04001487cb738da9f` |
| [Devkron-2.0-Windows-x64.zip](2.0-LTS/2.0.0/Devkron-2.0-Windows-x64.zip) | Windows x64 | `afcaaa71e01c3d0d30772430db276fff45572e23737e04125c821d921ff30ec7` |

Bibliotecas con código de terceros (opcionales, se descomprimen en la carpeta de `dkl`):
[csv](2.0-LTS/2.0.0/thirdparty/dkl2-csv-1.0.0.zip), [office](2.0-LTS/2.0.0/thirdparty/dkl2-office-1.0.0.zip),
[image](2.0-LTS/2.0.0/thirdparty/dkl2-image-1.0.0.zip), [html](2.0-LTS/2.0.0/thirdparty/dkl2-html-1.0.0.zip),
[markdown](2.0-LTS/2.0.0/thirdparty/dkl2-markdown-1.0.0.zip). Sumas en [SHA256SUMS](2.0-LTS/2.0.0/SHA256SUMS);
versiones y commits en [manifest.json](2.0-LTS/2.0.0/manifest.json).

## Verificar y descomprimir

```
cd 2.0-LTS/2.0.0 && sha256sum -c SHA256SUMS
unzip Devkron-2.0-Linux-x64.zip -d /opt          # Windows: Expand-Archive Devkron-2.0-Windows-x64.zip C:\
/opt/Devkron-2.0-Linux-x64/dkl -license          # sin licencia de 2.0 queda en modo demostración
```

## Versiones

Cada línea LTS tiene su carpeta y cada distribución su subcarpeta, que nunca se sobrescribe: `2.0-LTS/2.0.0/`,
`2.0-LTS/2.0.1/`, `2.0-LTS/2.0.2/`… (una línea futura sería `2.1-LTS/2.1.1/`). Los zips conservan el nombre de la
línea (`Devkron-2.0-<SO>-x64.zip`). La versión vigente es la más alta de la línea.

## Documentación

- [Descargas y contenido de los paquetes](https://docs.induxsoft.net/es/devkron/2.0/instalacion/descargas.md)
- Instalación: [Linux](https://docs.induxsoft.net/es/devkron/2.0/instalacion/linux.md) ·
  [Windows](https://docs.induxsoft.net/es/devkron/2.0/instalacion/windows.md)
- [Licencia](https://docs.induxsoft.net/es/devkron/2.0/instalacion/licencia.md)
- [dklwebsvr](https://docs.induxsoft.net/es/devkron/2.0/instalacion/dklwebsvr.md) ·
  [IIS (iis2dkl)](https://docs.induxsoft.net/es/devkron/2.0/instalacion/iis.md) ·
  [w3se](https://docs.induxsoft.net/es/productos/tools/w3se/) ·
  [httptn](https://docs.induxsoft.net/es/productos/tools/httptn/)
- [Devkron](https://docs.induxsoft.net/es/devkron/)
