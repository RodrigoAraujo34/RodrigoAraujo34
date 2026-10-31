<div align="center">

[Português](README.md) · [English](README_EN.md) · [Español](README_ES.md)

# Rodrigo Araújo — CesnnaBravo
### Mods para Euro Truck Simulator 2 y American Truck Simulator

![Versión](https://img.shields.io/badge/ETS_BRAKE_FADE-0.7.3.1-5965F2?style=for-the-badge)
![Plataforma](https://img.shields.io/badge/Windows-x64-0078D4?style=for-the-badge)
![Estado](https://img.shields.io/badge/ESTADO-BETA-F5A623?style=for-the-badge)

[Descarga oficial](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link) · [Discord](https://discord.gg/yFgebpcX8) · [Instagram](https://instagram.com/rodrigoaraujoca2/) · [Apoyar el desarrollo](https://buymeacoffee.com/cesnnabravo)

</div>

## Sobre el proyecto

Soy Rodrigo Araújo Campos, conocido como CesnnaBravo. Desarrollo mods y plugins DLL para ETS2 y ATS, utilizando IA como herramienta de apoyo. Me centro en la simulación, la dificultad y la inmersión.

**ETS BRAKE FADE** simula la temperatura de los frenos y la pérdida de eficacia causada por el sobrecalentamiento. Las frenadas repetidas o prolongadas acumulan calor; el enfriamiento recupera gradualmente la eficacia térmica. La masa de la carga, la velocidad, el desgaste del chasis y la pendiente estimada influyen en el modelo.

La temperatura mostrada es **calculada por el mod**, no una medición real de discos o tambores individuales. Esta versión no incluye un sistema de sobrepeso ni un sistema independiente de desgaste/mantenimiento de frenos.

## Novedades de la 0.7.3.1

- **Panel claro o negro**, con el tema guardado y la interfaz en portugués, inglés y español.
- **Ajustes térmicos:** temperatura de inicio del ruido, velocidad de calentamiento y de enfriamiento.
- **Monitor de frenos:** temperatura simulada, eficacia, carga y pendiente estimada.
- **Teclado, mando y volante en una sola DLL**, seleccionables en el panel.
- **ETS2 y ATS:** identificación del juego y calibración guardada en su carpeta correspondiente.
- **Nombre del dispositivo/eje en el juego:** `ETS BRAKE FADE 0.7.3.1`. Se conserva el identificador interno para mantener las asignaciones existentes.
- **Comprobador de actualizaciones**, compatible con versiones de tres o cuatro números. El aviso requiere una versión superior publicada en el servidor; la instalación sigue siendo manual.

### Correcciones incluidas

| Área | Corrección |
|---|---|
| Carga en Windows | Runtime C++ incorporado en la DLL, eliminando las dependencias externas de Visual C++ relacionadas con el caso reportado de error `0000007E`. |
| Panel térmico | Deslizadores dibujados por el propio panel para corregir barras vacías; admiten arrastre, teclado y reapertura. |
| Indicador de freno del juego | Lectura del pedal/S en las opciones mientras la conducción está pausada, sin avanzar la simulación térmica. |
| Calibración | Validación de finalización, recorrido, sentido y valores; los archivos inválidos no se consideran calibrados. |
| Pedales | Persistencia de los ejes Slider 1/2 e intento de recuperación tras perder la lectura. |
| Guardado | Archivo temporal antes de reemplazar la calibración y diagnóstico si no se puede guardar. |
| ATS | Calibración separada de ETS2 y selección de la ventana mediante el proceso que cargó el plugin. |
| Entrada/inicio | Resincronización del eje, F9 limitado a la ventana del juego y diagnóstico si falla el registro de eventos esenciales del SDK. |
| Simulación | Tratamiento de telemetría inválida para evitar corromper de forma persistente la temperatura o la salida del freno. |

**El humo de los frenos no forma parte de esta actualización.** El experimento está aplazado y desactivado en la distribución normal.

## Descarga

Utiliza la [carpeta oficial de descargas](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link) y comprueba que el ZIP sea la **0.7.3.1**. La carpeta puede contener versiones anteriores. El sitio web está en preparación; la carpeta anterior sigue siendo la referencia para descargar.

## Instalación — Windows de 64 bits

1. Cierra el juego y guarda una copia de la DLL anterior fuera de `plugins`.
2. Extrae el paquete. Copia **`ets2_brake_fade.dll`** y **`sounds`** a la carpeta correspondiente:

```text
Euro Truck Simulator 2\bin\win_x64\plugins
American Truck Simulator\bin\win_x64\plugins
```

3. Crea `plugins` si no existe. Mantén **solo una DLL de Brake Fade** en cada instalación.
4. Conserva `brake_fade_v07.ini` para mantener tus preferencias. Si probaste el humo, retira `cb_brake_smoke_probe.dll` y reemplaza el host experimental por la DLL normal.
5. Inicia el juego, carga un perfil/partida y entra en la conducción. Abre el panel con **F10** o tu atajo guardado.

El archivo `ets2_brake_fade.dll` es el mismo para ambos juegos; no es exclusivo de ETS2. Se instala junto al ejecutable según las rutas indicadas, no como archivo `.scs` en el Gestor de Mods.

## Teclado, mando y volante

| Tecla predeterminada | Función |
|---|---|
| F10 | Abrir/cerrar el panel. Configurable. |
| F7 | Avanzar la calibración de mando/volante. Configurable. |
| F9 | Enviar un pulso para asignar el eje virtual al freno. Fija. |
| S | Freno en modo Teclado. Fija. |
| Esc | Cerrar el panel o cancelar la captura de un atajo. |

### Teclado

Selecciona **Teclado** en el panel. Mantén **S** para frenar y suéltala para liberar. No necesitas mando ni calibración.

Asigna el **eje virtual** al freno del juego: selecciona el campo **Eje del freno** y pulsa F9. Elimina la asignación digital original de S al freno para evitar que aplique frenado en paralelo y anule el efecto de fade.

Durante la conducción, el plugin ignora S fuera de la ventana del juego o con su panel abierto. Al volver de una pausa o cambiar de modo, suelta S antes de pulsarla otra vez.

### Mando, volante y pedales

Selecciona **Mando/volante** y comprueba el atajo de calibración guardado. Durante la conducción, con el panel cerrado:

1. Suelta completamente el freno; pulsa y suelta el atajo de calibración.
2. Pisa **solo el freno** hasta el 100%, mantenlo y pulsa el atajo nuevamente.
3. Suelta completamente el freno y pulsa el atajo por tercera vez.
4. Comprueba la finalización y el guardado en **Diagnóstico**.
5. Selecciona **Eje del freno** en las opciones del juego y usa F9 para asignar el eje virtual.

Comprueba la polaridad: el indicador debe quedar en reposo al soltar el pedal y aumentar al pisarlo. **Conserva Normal/Invertido si ya funciona correctamente en tu perfil.** Nunca asignes Brake Fade a la dirección.

Los archivos antiguos sin confirmación de calibración completada requieren recalibrar una vez. Se pueden reutilizar archivos válidos de la revisión de estabilidad. La compatibilidad depende de que el controlador exponga un eje analógico legible; no se garantiza para todos los dispositivos.

### Ubicación de los archivos

| Archivo | Ubicación |
|---|---|
| Preferencias y atajos | `brake_fade_v07.ini`, junto a la DLL. |
| Registro del plugin | `brake_fade_v07.log`, junto a la DLL. |
| Calibración ETS2 | `Documentos\Euro Truck Simulator 2\BrakeFade\wheel_config.ini` |
| Calibración ATS | `Documentos\American Truck Simulator\BrakeFade\wheel_config.ini` |

Las rutas siguen la ubicación de Documentos configurada en Windows. ETS2 y ATS tienen calibraciones separadas. Si una versión antigua de ATS guardó en la carpeta de ETS2, recalibra en ATS; no hace falta borrar el archivo de ETS2.

## Personalizar los frenos

En **Ajustes térmicos**:

| Ajuste | Rango | Predeterminado |
|---|---|---|
| Temperatura de inicio del ruido | 50–500 °C | 100 °C |
| Velocidad de enfriamiento | 25–200% | 100% |
| Velocidad de calentamiento | 25–200% | 100% |

**Mayor porcentaje = más rápido; menor porcentaje = más lento.** Son tasas, no tiempos en segundos. El ruido requiere frenar en movimiento y aumenta gradualmente por encima del umbral.

El 100% conserva el ajuste de enfriamiento lento. En una prueba del modelo sin frenar, bajar de 500 °C a 150 °C tardó unos **6min30s detenido** y **3min43s a 80 km/h**. Son referencias del tiempo activo de la simulación, no mediciones de un camión real; las frenadas y otros ajustes cambian el resultado.

El botón **Tema: claro / Tema: oscuro** está en la parte inferior de la barra lateral. También se pueden ajustar volumen, idioma, avisos y simulación. Las preferencias se guardan automáticamente.

## Solución de problemas y soporte

- **No aparece el panel ni los avisos:** revisa `game.log.txt`. `unable to load: 0000007E` ocurre antes de iniciar el plugin. Usa el paquete actualizado; incorpora el runtime C++ y elimina las dependencias externas de Visual C++ de la compilación anterior. Si persiste, envía un registro nuevo.
- **No frena:** comprueba el modo, la calibración y la asignación del eje virtual al freno. Prueba el indicador en las opciones del juego.
- **Dirección brusca con A/D:** revisa las asignaciones y el tipo de control del juego. El eje virtual del mod debe actuar solo sobre el freno.
- **La calibración no se guarda:** revisa Diagnóstico y envía el registro. Puede funcionar en la sesión actual y requerir repetirla al reiniciar si el guardado falló.
- **Sin audio:** comprueba volumen, simulación activada, salida de Windows y `sounds`. Los WAV usan PCM de 16 bits, mono o estéreo. El audio procedural puede funcionar sin los WAV.
- **Sin aviso superpuesto:** prueba Ventana o Ventana sin bordes. La pantalla completa exclusiva puede impedir que aparezca.

En [Discord](https://discord.gg/yFgebpcX8), indica las versiones del mod y del juego, equipo, modo de entrada y pasos para reproducir el problema. Envía `game.log.txt` y `brake_fade_v07.log` del intento afectado. El registro del juego suele estar en Documentos, en la carpeta de ETS2/ATS, o en el `-homedir` personalizado.

La compilación x64 y **ocho pruebas automatizadas** pasaron, incluyendo carga de la DLL, identificación ATS/ETS2, dependencias, calibración, idiomas, entrada, física térmica y panel. Los usuarios han confirmado las correcciones de los casos reportados; esto no garantiza ausencia de fallos en todas las configuraciones.

## Tutoriales en vídeo

[Tutorial 1](https://www.youtube.com/watch?v=pR7P1BxTyl8) · [Tutorial 2](https://www.youtube.com/watch?v=25W1FI4E_3o&t=205s)

Los vídeos pueden mostrar versiones anteriores. Para atajos, instalación y calibración de la 0.7.3.1, sigue este README.

## Historial de versiones

| Versión | Cambios principales |
|---|---|
| **0.7.3.1** | Temas claro/oscuro, ajustes térmicos, monitor, correcciones del panel/calibración/entrada, soporte ATS revisado y carga sin dependencias externas de Visual C++. |
| 0.7 | Modos de entrada unificados, panel rediseñado, tres idiomas, atajos y diagnóstico. |
| 0.6 | Audio dinámico y transiciones suaves. |
| 0.5 | Ajustes de enfriamiento e influencia de carga/desgaste del chasis. |
| 0.4 | Avisos de temperatura, calibración y preferencias guardadas. |
| 0.3 | Mayor soporte de dispositivos de entrada. |

## Próximas mejoras — en estudio

- Continuar corrigiendo fallos con los registros y comentarios de la comunidad.
- Ampliar las pruebas con volantes, pedales y mandos en ETS2 y ATS.
- Refinar diagnóstico, interfaz y comportamiento térmico según los jugadores.
- Retomar la investigación de humo en los frenos después de la fase de estabilidad. El prototipo actual es diagnóstico y **no emite partículas visuales**.

Estos puntos no son funciones disponibles ni promesas de fechas o compatibilidad. La prioridad actual es la estabilidad.

Las versiones antiguas que solo reconocen tres números no detectan automáticamente `0.7.3.1`; esta migración es manual. El comprobador de esta versión reconoce tres o cuatro componentes y no instala DLLs automáticamente.

## Apoyar el desarrollo

El mod es gratuito. Las donaciones son opcionales y no hacen falta para descargarlo ni utilizarlo.

[Buy Me a Coffee](https://buymeacoffee.com/cesnnabravo)

PIX — clave aleatoria, Rodrigo Araújo Campos:

```text
c2ad1129-8267-4e80-a0b6-2e0ddb93526c
```

[Instagram](https://instagram.com/rodrigoaraujoca2/) · [Discord](https://discord.gg/yFgebpcX8) · [GitHub](https://github.com/RodrigoAraujo34/RodrigoAraujo34)

**Realismo • Simulación • Inmersión — CesnnaBravo**
