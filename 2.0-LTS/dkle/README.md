# Devkron Edge (dkle)

Runtime gratuito del lenguaje Devkron (DKL) para microservicios y conectores entre API HTTP: un solo ejecutable, sin
dependencias, con su propio servidor HTTP/HTTPS (y FastCGI) y cambios en caliente. Tiene su propio ciclo de versiones,
aparte del motor de Devkron 2.0.

## Versión vigente: 2.0.1

| Archivo | Plataforma | SHA-256 |
|---|---|---|
| [dkle-2.0.1-Linux-x64.zip](2.0.1/dkle-2.0.1-Linux-x64.zip) | Linux x64 | `6026c569c593bf245991d636b49f1b96650288b167cc71ee0b7cd9f4edf3a25f` |
| [dkle-2.0.1-Linux-arm64.zip](2.0.1/dkle-2.0.1-Linux-arm64.zip) | Linux ARM64 | `03ebd81ebca02d4938a34afd0879d64a46cf4f32ddfb7fac0a4738098f7dd74f` |
| [dkle-2.0.1-Windows-x64.zip](2.0.1/dkle-2.0.1-Windows-x64.zip) | Windows x64 | `62ed0e9f50949cabec76fd953cc6d914dfacbe0a4daa42f9ffaab744670c9ea9` |

Sumas en [SHA256SUMS](2.0.1/SHA256SUMS); versión, commit y dependencias en [manifest.json](2.0.1/manifest.json).

## Verificar y probar

```
cd 2.0-LTS/dkle/2.0.1 && sha256sum -c SHA256SUMS
unzip dkle-2.0.1-Linux-x64.zip
cd dkle-2.0.1-Linux-x64/ejemplo && ../dkle run --root . GET /hola
```

## Versiones

Cada versión de `dkle` va en su propia carpeta (`2.0-LTS/dkle/2.0.1/`, `2.0-LTS/dkle/2.0.2/`…), que nunca se
sobrescribe. La vigente es la más alta.

## Documentación

- [Devkron Edge](https://docs.induxsoft.net/es/devkron/2.0/dkle/)
- [Instalación](https://docs.induxsoft.net/es/devkron/2.0/dkle/instalacion.md) ·
  [Configuración](https://docs.induxsoft.net/es/devkron/2.0/dkle/configuracion.md) ·
  [Programas y sitios](https://docs.induxsoft.net/es/devkron/2.0/dkle/programas.md) ·
  [Despliegue](https://docs.induxsoft.net/es/devkron/2.0/dkle/despliegue.md)
