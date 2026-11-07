# dkl-debug: depurador de Devkron (DKL)

Depurador para programas de Devkron 2.0 que habla Debug Adapter Protocol, así que funciona en VS Code, Cursor y VSCodium
con la [extensión de Devkron](../vscode/README.md). Es autocontenido: trae el motor del mismo commit y los `.dkh`
oficiales, sin necesidad de instalar Devkron. Tiene su propio ciclo de versiones, aparte del motor.

## Versión vigente: 0.1.1 (motor 2.0.5.0)

| Archivo | Plataforma | SHA-256 |
|---|---|---|
| [dkl-debug-0.1.1-Linux-x64.zip](0.1.1/dkl-debug-0.1.1-Linux-x64.zip) | Linux x64 | `421e93736d49459a0bf4be0edc337c9904a3644f186e2e3a9ef804953da12c6a` |
| [dkl-debug-0.1.1-Linux-arm64.zip](0.1.1/dkl-debug-0.1.1-Linux-arm64.zip) | Linux ARM64 (sin probar) | `beeeee55f04e5d9fa2d1079ea0cd70d8f12da7196d84a3cebd66501b2c5e69e5` |
| [dkl-debug-0.1.1-Windows-x64.zip](0.1.1/dkl-debug-0.1.1-Windows-x64.zip) | Windows x64 (sin probar) | `311c6c28f05cb730fb4e1ed7b552a4887654307491545d7959cf484c70728647` |

Sumas en [SHA256SUMS](0.1.1/SHA256SUMS); versión, commit y estado de las pruebas en [manifest.json](0.1.1/manifest.json).
0.1.1 es 0.1.0 recompilado con el motor de Devkron 2.0.5.0: úselo con esa distribución. La anterior sigue en
[0.1.0](0.1.0/) (motor 2.0.2).

## Uso

```
cd 2.0-LTS/dkl-debug/0.1.1 && sha256sum -c SHA256SUMS
unzip dkl-debug-0.1.1-Linux-x64.zip -d /opt
/opt/dkl-debug-0.1.1-linux-x64/dkl-debug --version
/opt/dkl-debug-0.1.1-linux-x64/dkl-debug --check programa.dkl          # errores de sintaxis con la línea real
/opt/dkl-debug-0.1.1-linux-x64/dkl-debug programa.dkl --break programa.dkl:12
```

En VS Code o Cursor: instala la extensión, pon la ruta del ejecutable en el ajuste `devkron.debuggerPath` (o agrégalo
al PATH) y presiona F5 sobre un `.dkl`.

## Qué hace

- Puntos de interrupción por línea real, condicionales y de registro; paso a paso (entrar, sobre, salir); pila de
  llamadas; variables locales, globales y objetos (registros y listas expandibles, alias de los bloques `go`);
  evaluar expresiones; detenerse en excepciones.
- `--check [--json]`: errores de sintaxis con la línea y la columna reales (los mensajes de `dkl` pueden traer la línea
  desfasada).

## Limitaciones de 0.1.x

Sin depuración de sitios web (FastCGI) todavía; solo el hilo principal; los paquetes cifrados se ejecutan sin
detenerse; la compilación nativa se apaga mientras depura.

## Versiones

Cada versión va en su propia carpeta (`2.0-LTS/dkl-debug/0.1.0/`, `0.1.1/`…), que nunca se sobrescribe. La vigente es
la más alta.
