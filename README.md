# Dragon Ball: Shen Long no Nazo — Traducción al castellano

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/nes/dragon-ball-shen-long-no-nazo)**.

Traducción al **español de España** de *Dragon Ball: Shen Long no Nazo*
(Famicom, Bandai, 1986), el primer videojuego de Dragon Ball, hecha desde la
ROM japonesa original. En Occidente solo llegó como *Dragon Power*, con los
personajes y la historia cambiados; este parche conserva a Goku, Bulma, Oolong,
Yamcha, Mutenroshi y compañía tal y como aparecen en la versión japonesa.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu
propia copia para aplicarlo.

## Estado

Última versión: **[v1.0 — Guion, menús y títulos en castellano](../../releases/tag/v1.0)**.

| Parte | Estado |
|---|---|
| Guion | Las 566 líneas del juego traducidas del japonés: los diálogos de las 217 escenas, las narraciones de la demo, los menús de deseos de Shen Long y el final |
| Títulos de capítulo | Los 14 traducidos |
| Interfaz | Empezar, Continuar, Récord, Puntos y Fin de la partida |
| Fuente | Nueva fuente española con minúsculas, tildes, diéresis, eñe, ¡ y ¿, dibujada con el mismo trazo y el mismo contraste que las mayúsculas originales del juego |
| Rótulos gráficos | Se conservan el logotipo DRAGON BALL, el rótulo 神龍の謎 y los créditos: forman parte de la imagen de marca del juego |
| Compatibilidad | La ROM resultante conserva tamaño y mapper (GxROM), así que sirve también en cartucho |

### Comprobaciones y trabajo pendiente

Cada línea traducida se ha vuelto a leer desde la ROM construida y coincide
con el guion. Todas las escenas se han forzado en el emulador (fceumm mediante
libretro) y su texto se ha leído tile a tile en pantalla para comprobar que
cada línea aparece completa, en su fila y dentro del bocadillo. Se han
comprobado además el título, la demo con las narraciones, la pantalla de
capítulo y marcador, las primeras escenas jugando y varios títulos de capítulo.

**Falta una partida completa de principio a fin** y la prueba en consola
física. Las comprobaciones hechas no acreditan cada pantalla del juego en su
contexto real de juego.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **japonesa**. El parche solo funciona
   con esa versión exacta.
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Dragon Ball - Shen Long no Nazo (Japan).nes` |
   | Tamaño | 163.856 bytes (con cabecera iNES) |
   | CRC32 | `2506FB77` |
   | MD5 | `b5b0d9a7624f12e39ca0048ffe6b7b77` |
   | SHA-256 | `2a7e4c99771c4292cc9d1261a01af1d93f4d94e6865d1c257e2a19fc4dca6451` |

   ```bash
   md5sum "Dragon Ball - Shen Long no Nazo (Japan).nes"     # Linux
   md5 "Dragon Ball - Shen Long no Nazo (Japan).nes"        # macOS
   CertUtil -hashfile "Dragon Ball - Shen Long no Nazo (Japan).nes" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto. No sirve
   *Dragon Power* (USA) ni una ROM ya modificada.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "juego original.nes" parche.xdelta "juego traducido.nes"`
5. Comprueba que la ROM resultante tiene **163.856 bytes** y MD5
   **`4a01f80f8a57160f53b1af7436f25213`** (SHA-256 `9e96e97f8cabbdbcdd6ddb07121c47f39795288694346b204981655db385f9d1`).
6. Carga la ROM resultante en tu emulador o flashcard preferidos y empieza una
   partida nueva.

Aplica cada versión sobre la **ROM japonesa original**, no sobre una ROM ya
traducida.

## Errores

Para comunicar un error, abre una incidencia con la versión del parche, el
emulador, el capítulo y la frase o pantalla afectada. No adjuntes la ROM.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin
relación alguna con Bandai, Bird Studio, Shueisha, Fuji TV ni Toei Animation.
Aquí no se distribuye el juego ni ninguna parte de él: solo un parche que
modifica una copia que ya tengas. Este repositorio contiene únicamente el
README; el parche está en Releases.

Si eres el titular de los derechos y quieres que retire esto, abre una
incidencia y lo hago.
