<div align="center">

[Português](README.md) · [English](README_EN.md) · [Español](README_ES.md)

# Rodrigo Araújo — CesnnaBravo
### ETS BRAKE FADE 0.8.0

![Versión](https://img.shields.io/badge/ETS_BRAKE_FADE-0.8.0-5965F2?style=for-the-badge)
![Plataforma](https://img.shields.io/badge/Windows-x64-0078D4?style=for-the-badge)

[Sitio oficial](https://cb-mods-road.wswmjkwr2r.chatgpt.site/) · [Descargas](https://cb-mods-road.wswmjkwr2r.chatgpt.site/#mods) · [Discord](https://discord.gg/yFgebpcX8)

</div>

> **AVISO — NOS TRASLADAMOS AL SITIO OFICIAL**
>
> El [sitio CB Mods](https://cb-mods-road.wswmjkwr2r.chatgpt.site/) es ahora la central del proyecto: descargas actualizadas, tutoriales, registro, biblioteca y compra del complemento de humo. Este GitHub continúa como presentación y referencia para la comunidad. Descarga la versión actual desde el sitio; los archivos antiguos pueden no corresponder a la distribución vigente.

## Sobre el proyecto

Soy Rodrigo Araújo Campos, conocido como CesnnaBravo. Desarrollo mods con apoyo de IA para añadir simulación e inmersión a los viajes.

**ETS BRAKE FADE** simula calentamiento, enfriamiento y pérdida de eficacia de los frenos, con datos separados para el camión y los remolques. Las temperaturas, masas y potencias son **estimaciones del modelo**, con un perfil térmico genérico; no son mediciones reales ni datos de fabricante.

## Novedades de la 0.8.0

- Temperaturas y pérdida de capacidad independientes por vehículo, con recuperación al enfriarse.
- Masa bruta estimada del conjunto, carga, velocidad y pendiente en el cálculo térmico.
- Controles originales del juego para teclado, mando y volante: **sin calibrar el plugin ni utilizar F9**.
- Panel claro/oscuro, portugués/inglés/español, audio y avisos.
- Tasas de calentamiento y enfriamiento ajustables entre **25% y 200%**. Mayor porcentaje significa más rápido.
- Complemento **Brake Smoke** con humo en el camión y los remolques conectados, perfiles detenido/en movimiento, densidad ajustable y botón de activación.
- Vinculación de la cuenta mediante el navegador y verificación del acceso al humo en el servidor.
- Avisos de nuevas versiones publicadas en el sitio. La instalación sigue siendo manual.

### Curva de pérdida de eficacia

| Temperatura estimada | Ganancia del freno de servicio del vehículo afectado |
|---|---|
| Hasta 350 °C | 100% |
| 440 °C | 50% |
| 530 °C o más | 0% |

La reducción es progresiva entre 350 y 530 °C. Camión y remolques se calculan por separado. La capacidad se recupera al enfriarse; se conservan el freno de estacionamiento y los auxiliares. Esta curva es un ajuste del mod, no una especificación de frenos reales.

## Base gratuita y humo de pago

| Producto | Acceso |
|---|---|
| **ETS Brake Fade — base** | Gratuita; los frenos funcionan sin iniciar sesión. |
| **Brake Smoke — complemento** | **R$ 15 BRL**, pago único en el sitio. Requiere una cuenta con acceso habilitado, verificación en línea y SCS activo. |

La compra confirmada habilita el complemento en la biblioteca de la cuenta. El panel se vincula con un código autorizado en el sitio; la contraseña no se guarda en el plugin. Las cuentas con acceso concedido manualmente por el administrador también pueden usarlo.

Sin verificación en línea, el humo queda bloqueado; los frenos gratuitos siguen disponibles. La densidad va de **0% a 500%** y se puede desactivar desde el panel. La emisión se solicita a partir de **420 °C** por vehículo y cesa al enfriarse a **380 °C o menos**, con disipación gradual de las partículas.

## Compatibilidad actual

**Windows x64 · ETS2 1.62.1.0 — ejecutable reconocido por la integración nativa.**

**American Truck Simulator: compatibilidad en preparación.** No utilices ni compres la 0.8.0 y su complemento esperando compatibilidad con ATS. Otras versiones del juego también requieren adaptación y validación. El soporte de versiones anteriores del plugin no garantiza el del sistema nuevo.

## Instalación y actualización

1. Cierra el juego y guarda una copia anterior fuera de `plugins`.
2. Descarga la base actual en el sitio. Copia el contenido de `plugins` a `Euro Truck Simulator 2\bin\win_x64\plugins`.
3. Mantén **las dos DLL**: `ets2_brake_fade.dll` y `cb_brake_smoke_probe.dll`, además de `cb_smoke_native.ini` y `sounds`. Pese a su nombre antiguo, la segunda DLL ejecuta física y partículas y es necesaria.
4. Retira DLL antiguas duplicadas y el diagnóstico `cb_brake_physics_probe.dll`. Conserva `brake_fade_v07.ini` para mantener tus preferencias.
5. Utiliza los controles originales del juego. Elimina la asociación al eje virtual antiguo si existe. Abre el panel con **F10** o tu atajo guardado.
6. Para el humo, copia también el SCS del complemento a `Documentos\Euro Truck Simulator 2\mod`, actívalo en el Gestor de Mods y vincula tu cuenta desde el panel. Utiliza la ubicación de Documentos configurada en Windows.

**Tutoriales completos del sitio (portugués):** [instalar la base gratuita](https://cb-mods-road.wswmjkwr2r.chatgpt.site/install-base.html) · [instalar y activar el humo](https://cb-mods-road.wswmjkwr2r.chatgpt.site/install-smoke.html)

## Soporte y próximas mejoras

En [Discord](https://discord.gg/yFgebpcX8), indica versiones del juego/mod, equipo, pasos del problema, `game.log.txt` y `brake_fade_v07.log`. Nunca compartas contraseñas ni `account.dat`.

Las prioridades son estabilidad, pruebas con más conjuntos y adaptación a ATS. No se prometen fechas ni compatibilidad universal. Las pruebas automatizadas y los comentarios de jugadores no sustituyen la validación en cada versión del juego.

## Apoyar el desarrollo

La base es gratuita. Las donaciones son opcionales y están separadas de la compra del complemento de humo.

[Buy Me a Coffee](https://buymeacoffee.com/cesnnabravo) · [Instagram](https://instagram.com/rodrigoaraujoca2/) · [Discord](https://discord.gg/yFgebpcX8)

Clave PIX para donaciones — Rodrigo Araújo Campos: `c2ad1129-8267-4e80-a0b6-2e0ddb93526c`.

**Realismo • Simulación • Inmersión — CesnnaBravo**
