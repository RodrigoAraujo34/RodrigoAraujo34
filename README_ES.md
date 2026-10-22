<div align="center">

[![Português](https://img.shields.io/badge/Idioma-Português-009C3B?style=for-the-badge)](README.md)
[![English](https://img.shields.io/badge/Language-English-1E90FF?style=for-the-badge)](README_EN.md)
[![Español](https://img.shields.io/badge/Idioma-Español-EAA221?style=for-the-badge)](README_ES.md)

# 🚛 Rodrigo Araújo — CesnnaBravo

### Desarrollo de mods para ETS2 y ATS con ayuda de IA

![Versión](https://img.shields.io/badge/BRAKE_FADE-v0.7-8A2BE2?style=for-the-badge)
![Estado](https://img.shields.io/badge/ESTADO-BETA-F5A623?style=for-the-badge)
![Plataforma](https://img.shields.io/badge/Windows-64_bits-0078D4?style=for-the-badge&logo=windows&logoColor=white)

[Descargas](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link) · [Discord](https://discord.gg/yFgebpcX8) · [Instagram](https://instagram.com/rodrigoaraujoca2/) · [Apoyar el desarrollo](https://buymeacoffee.com/cesnnabravo)

</div>

## 👨‍💻 Sobre mí

Soy Rodrigo Araújo Campos, conocido como CesnnaBravo. Desarrollo plugins DLL y mods para Euro Truck Simulator 2 y American Truck Simulator, utilizando inteligencia artificial como herramienta de apoyo. Mis proyectos se centran en el realismo, la simulación, nuevas mecánicas y la inmersión.

## 🔥 Brake Fade v0.7

Brake Fade simula el calentamiento y la pérdida de eficacia de los frenos. La masa de la carga, la velocidad y el desgaste del chasis influyen en la simulación. El frenado continuo puede sobrecalentar los frenos y reducir gravemente su eficacia.

### 🆕 Novedades

- **Dos modos en una DLL:** elige Teclado o Mando/volante desde el panel.
- **Teclado:** mantén **S** para frenar y suéltala para liberar. No necesita mando ni calibración.
- **Mando/volante:** mantiene el pedal o gatillo analógico y la calibración guardada.
- **Nuevo panel F10:** navegación lateral, controles organizados, volumen, simulación y avisos.
- **Tres idiomas:** portugués de Brasil, inglés y español, aplicados inmediatamente al panel, avisos, calibración, diagnóstico e historial mostrado.
- **Atajos personalizables:** F7 y F10 son los valores predeterminados; F9 y S siguen siendo fijos.
- **Diagnóstico y registros:** estado de la sesión, modo de entrada, audio, calibración y copia del historial.
- **Preferencias guardadas:** modo, idioma, volumen, avisos, simulación y atajos.

Se mantienen el audio dinámico con WAV y textura procedural, las transiciones suaves, la simulación térmica, el enfriamiento y la influencia de la carga y del desgaste del chasis.

![Panel Brake Fade v0.7 con el modo teclado seleccionado](assets/brake-fade-v07-teclado.png)

*Captura real de la vista previa del panel, en portugués. Utiliza el selector de idioma para cambiar a español.*

## 📥 Descarga oficial

[**Abrir la carpeta oficial de descargas**](https://drive.google.com/drive/folders/10GtsLWKFm5A8UQ5ram_yBqZJTe6cOlUx?usp=drive_link)

**Comprueba que el paquete v0.7 esté disponible antes de descargarlo.** Actualizar este README no sube el paquete a Google Drive.

## 📦 Instalación

1. Cierra completamente ETS2/ATS.
2. En Steam, abre **Propiedades → Archivos instalados → Explorar** para localizar el juego.
3. Abre `bin\win_x64\plugins`; crea `plugins` si no existe.
4. Guarda una copia de las DLL antiguas de Brake Fade fuera de esa carpeta y retíralas de `plugins`.
5. Copia la DLL v0.7 y la carpeta `sounds` del paquete a `plugins`.
6. Inicia el juego, carga el perfil y la partida y entra en el camión.
7. Pulsa **F10**, o tu atajo guardado, para abrir el panel.

```text
bin/win_x64/plugins/
├── ets2_brake_fade.dll
└── sounds/
    ├── audio carreta temperatura baixa.wav
    └── audio_carreta temperatura alta.wav
```

El nombre de la DLL puede variar; la compilación del proyecto también puede llamarse `ets2_brake_fade_wheel.dll`. **Instala solamente una DLL de Brake Fade.** La versión integrada incluye ambos modos aunque el nombre contenga `wheel`. No cambies los nombres de los WAV.

Es un plugin DLL, no un archivo `.scs` para activar en el Gestor de Mods.

## 🎯 Asignar el eje virtual — obligatorio en ambos modos

1. Cierra el panel del mod y abre **Opciones → Controles** del juego.
2. Haz clic en el campo de asignación de **Eje del freno**.
3. Sin accionar pedales o gatillos, pulsa **F9** una vez.
4. Comprueba que se asigna el eje de Brake Fade. Puede aparecer como **ETS2 Brake Fade / Brake Fade Pedal**.
5. Configura el modo del eje como **Normal**.

El juego debe usar el **eje virtual**, no el eje físico del freno directamente. Así recibe el frenado reducido por la simulación. F9 asigna el eje; no calibra el equipo.

### ⌨️ Teclado

1. En **Configuración → Teclas y controles**, selecciona **Teclado**.
2. Retira **S** del comando digital original de freno de servicio en **Teclas y botones** del juego.
3. Mantén asignado el eje virtual mediante F9.
4. Vuelve a la conducción, cierra el panel, suelta S y luego mantenla para frenar.

No necesitas conectar un mando ni calibrar. El plugin sigue leyendo S aunque retires la asignación digital del juego. Mantener ese comando original puede aplicar frenado en paralelo e impedir que notes la pérdida de eficacia.

S solicita frenado total, limitado por la eficacia actual. Después de una pausa, cambio de ventana o cambio de modo, suelta S antes de volver a pulsarla. El modo teclado ignora S fuera del juego, con el panel abierto y durante la pausa.

### 🛞 Volante y pedales

1. Conecta el equipo antes de iniciar el juego y comprueba su reconocimiento en Windows.
2. Selecciona **Mando/volante** en el panel.
3. Detén el camión, vuelve a la conducción y cierra el panel del mod.
4. **Suelta totalmente el freno y pulsa F7.**
5. **Pisa solamente el freno al 100%, mantenlo y pulsa F7 otra vez.**
6. **Suéltalo completamente y pulsa F7 por tercera vez.**
7. Comprueba el mensaje de calibración completada.
8. Asigna el eje virtual con F9, en modo Normal, y prueba a baja velocidad.

No muevas otros pedales o ejes durante la calibración. La dirección, el acelerador y el embrague pueden conservar sus asignaciones físicas habituales. Si cambiaste el atajo de calibración, utiliza esa tecla en lugar de F7.

### 🎮 Mando / gamepad

Selecciona **Mando/volante** y calibra el gatillo o eje analógico del freno siguiendo las mismas etapas: **suelto → F7; totalmente presionado → F7; suelto → F7**. Hazlo en la conducción con el panel cerrado.

Después asigna el eje virtual con F9 y modo Normal. Retira comandos digitales de freno que puedan actuar en paralelo. No muevas las palancas ni otros gatillos durante la calibración. Un control presentado solamente como botón digital puede no ser detectado como eje del freno.

### 🔄 Cambiar de modo y recalibrar

Detén el camión, suelta los controles de frenado y selecciona el modo en el panel. La opción se guarda y la calibración del volante/mando se conserva. El mismo eje virtual sirve para los dos modos.

Si ya existe una calibración activa, el atajo inicia una nueva calibración. Sigue las instrucciones para presionar totalmente, confirmar, soltar y confirmar de nuevo. Si vienes de la antigua DLL exclusiva de teclado, revisa la asignación F9: el dispositivo integrado conserva el identificador de la versión de volante.

## ⌨️ Atajos e idiomas

| Tecla predeterminada | Acción |
|:---:|:---|
| F10 | Abrir/cerrar panel |
| F7 | Calibrar/recalibrar mando o volante |
| F9 | Asignar eje virtual; fija |
| S | Frenar con teclado; fija |
| Esc | Cerrar panel o cancelar cambio de atajo |

Puedes cambiar F7/F10 por teclas entre F1 y F12, excepto F9. Los dos atajos deben ser diferentes. **Restaurar atajos predeterminados** devuelve F7/F10.

En **Idioma / Language**, elige Português (Brasil), English (US) o Español. El cambio es inmediato y queda guardado. Los identificadores técnicos, nombres de archivos y códigos de error no cambian. Las líneas ya escritas en el archivo de registro conservan el idioma utilizado al guardarlas.

## 🌡️ Temperatura, carga y desgaste

| Temperatura | Eficacia térmica |
|:---:|:---:|
| Hasta 150 °C | 100% |
| 200 °C | 95% |
| 250 °C | 85% |
| 300 °C | 70% |
| 350 °C | 50% |
| 400 °C | 30% |
| 450 °C | 15% |
| 500 °C o más | 0% |

La eficacia cambia progresivamente entre esos puntos. El desgaste del chasis también limita la eficacia final. Los avisos comienzan a 300, 350, 400, 450 y 500 °C. Tras un aviso de calentamiento, la recuperación se anuncia al bajar a 150 °C o menos.

La masa de la carga recibida por telemetría influye en el calentamiento. La velocidad afecta al calentamiento y al enfriamiento. Utiliza el freno motor, el retarder cuando esté disponible y planifica las frenadas dentro del juego.

## 🛠️ Solución de problemas

| Problema | Qué comprobar |
|:---|:---|
| El panel no abre | Carpeta correcta, DLL extraída, juego reiniciado, atajo guardado y tecla Fn si corresponde. |
| Esperando perfil/partida | Carga la partida y entra en la conducción. |
| S no frena | Modo Teclado, eje virtual asignado, juego en primer plano, panel cerrado y S suelta antes de pulsarla de nuevo. |
| Falla la calibración | Eje analógico reconocido, modo Mando/volante, panel cerrado y únicamente el freno en movimiento. |
| El freno queda accionado | Recalibra, selecciona modo Normal y retira asignaciones en conflicto. |
| No se nota la pérdida de eficacia | Simulación activada, eje virtual asignado y ningún freno físico/digital actuando en paralelo. |
| F9 no asigna | Haz clic primero en el campo Eje del freno; comprueba Fn + F9 si hace falta. |
| Falta audio | Volumen del mod, simulación activada, salida de Windows, carpeta y nombres exactos de los WAV; PCM 16 bits mono/estéreo. |
| No se ven los avisos | Prueba Ventana o Ventana sin bordes. La pantalla completa exclusiva no está garantizada. |

La textura procedural puede sonar aunque falten las capas WAV. Escuchar algún sonido no confirma que ambos archivos se hayan cargado.

## 💬 Soporte

Consulta **Diagnóstico** y **Registros** en el panel. Indica juego y versión, Brake Fade v0.7, modo, equipo, pasos para reproducir y una captura o los registros copiados.

- `brake_fade_v07.log`: junto a la DLL.
- `game.log.txt`: normalmente en `Documentos\Euro Truck Simulator 2` o `Documentos\American Truck Simulator`, o en tu carpeta `-homedir`.
- [Discord de soporte y comunidad](https://discord.gg/yFgebpcX8)

Las preferencias se guardan en `brake_fade_v07.ini`, junto a la DLL. La calibración del volante/mando se almacena por separado.

## 🎥 Tutoriales en vídeo

[Tutorial 1](https://www.youtube.com/watch?v=pR7P1BxTyl8) · [Tutorial 2](https://www.youtube.com/watch?v=25W1FI4E_3o&t=205s)

Los vídeos pueden mostrar versiones anteriores. Para los modos y atajos personalizables de v0.7, sigue este README.

## 📜 Historial

- **v0.7 — Beta actual:** modos integrados, nuevo panel, tres idiomas, atajos personalizables, diagnóstico y preferencias guardadas.
- **v0.6:** audio dinámico, transiciones suaves, F7 como calibración predeterminada y F9 para asignar el eje.
- **v0.5:** audio anterior, enfriamiento revisado e influencia del desgaste y la carga.
- **v0.4:** avisos, visualización de eficacia, confirmación de calibración y ajustes guardados.
- **v0.3:** compatibilidad ampliada con dispositivos de entrada.

Es una beta. Se verificaron la compilación, los controles automatizados y la vista previa del panel; la validación dentro del juego con diferentes equipos y configuraciones continúa con los jugadores.

## 💜 Apoya el desarrollo

Brake Fade es gratuito. Las donaciones son opcionales y no son necesarias para descargar ni utilizar el mod.

[Buy Me a Coffee](https://buymeacoffee.com/cesnnabravo)

PIX — clave aleatoria, Rodrigo Araújo Campos:

```text
c2ad1129-8267-4e80-a0b6-2e0ddb93526c
```

También puedes apoyar dejando una ⭐ en [GitHub](https://github.com/RodrigoAraujo34/RodrigoAraujo34).

**Realismo • Simulación • Inmersión — Rodrigo Araújo Campos / CesnnaBravo**
