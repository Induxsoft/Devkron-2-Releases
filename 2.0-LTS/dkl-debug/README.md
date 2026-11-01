# dkl-debug: depurador de Devkron (DKL)

Depurador para programas de Devkron 2.0 que habla Debug Adapter Protocol, así que funciona en VS Code, Cursor y VSCodium
con la [extensión de Devkron](../vscode/README.md). Es autocontenido: trae el motor del mismo commit y los `.dkh`
oficiales, sin necesidad de instalar Devkron. Tiene su propio ciclo de versiones, aparte del motor.

## Versión vigente: 0.1.0 (motor 2.0.2)

| Archivo | Plataforma | SHA-256 |
|---|---|---|
| [dkl-debug-0.1.0-Linux-x64.zip](0.1.0/dkl-debug-0.1.0-Linux-x64.zip) | Linux x64 | `8c910091eb1d275031d3344d0c30a3946ee3c66aa30826b63eadec42f0c48378` |
| [dkl-debug-0.1.0-Linux-arm64.zip](0.1.0/dkl-debug-0.1.0-Linux-arm64.zip) | Linux ARM64 (sin probar) | `1281c52570d66a71647b3536191d2cbfe724a6d41983a626985b2da10e564c53` |
| [dkl-debug-0.1.0-Windows-x64.zip](0.1.0/dkl-debug-0.1.0-Windows-x64.zip) | Windows x64 (sin probar) | `2a95dd5fdc44ad50287653e49a30e701807ad39205f0e73de6bb391c9f708361` |

Sumas en [SHA256SUMS](0.1.0/SHA256SUMS); versión, commit y estado de las pruebas en [manifest.json](0.1.0/manifest.json).

## Uso

```
cd 2.0-LTS/dkl-debug/0.1.0 && sha256sum -c SHA256SUMS
unzip dkl-debug-0.1.0-Linux-x64.zip -d /opt
/opt/dkl-debug-0.1.0-Linux-x64/dkl-debug --version
/opt/dkl-debug-0.1.0-Linux-x64/dkl-debug --check programa.dkl          # errores de sintaxis con la línea real
/opt/dkl-debug-0.1.0-Linux-x64/dkl-debug programa.dkl --break programa.dkl:12
```

En VS Code o Cursor: instala la extensión, pon la ruta del ejecutable en el ajuste `devkron.debuggerPath` (o agrégalo
al PATH) y presiona F5 sobre un `.dkl`.

## Qué hace

- Puntos de interrupción por línea real, condicionales y de registro; paso a paso (entrar, sobre, salir); pila de
  llamadas; variables locales, globales y objetos (registros y listas expandibles, alias de los bloques `go`);
  evaluar expresiones; detenerse en excepciones.
- `--check [--json]`: errores de sintaxis con la línea y la columna reales (los mensajes de `dkl` pueden traer la línea
  desfasada).

## Limitaciones de 0.1.0

Sin depuración de sitios web (FastCGI) todavía; solo el hilo principal; los paquetes cifrados se ejecutan sin
detenerse; la compilación nativa se apaga mientras depura.

## Versiones

Cada versión va en su propia carpeta (`2.0-LTS/dkl-debug/0.1.0/`, `0.1.1/`…), que nunca se sobrescribe. La vigente es
la más alta.
