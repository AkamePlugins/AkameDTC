<p align="center">
  <img src="assets/akame-banner.png" alt="Akame Plugins" width="720">
</p>

# AkameDTC

Plugin de eventos **DTC (Destroy the Core)** para servidores **Paper 1.21**. Autor: **Motlys**.

Un bloque especial del mapa tiene una vida configurable. Cada golpe válido le resta 1 de vida y da 1 punto al jugador. Al terminar el evento, por tiempo o porque el bloque se destruye, se premia el ranking.

> El código fuente de este plugin es privado. Este repositorio es solo una presentación del proyecto.

## Características

- **Evento por estados:** sin configurar, desactivado, activo y en pausa, con transiciones controladas.
- **Ranking con empates:** las posiciones se comparten (1, 1, 3, 4).
- **Recompensas persistentes:** cada premio se registra en base de datos antes y después de ejecutarse, y las entregas interrumpidas se pueden revisar y reintentar a mano.
- **Horarios automáticos** con zona horaria y cambios de hora de verano, y cuenta atrás en horas y minutos hasta el próximo evento.
- **Interfaz:** BossBar, ActionBar y avisos globales de golpes, con sonidos configurables.
- **Hologramas opcionales** con FancyHolograms o DecentHolograms, y **PlaceholderAPI** opcional.
- **Recuperación tras reinicio:** el evento activo continúa donde estaba, con su puntuación.
- **Historial y estadísticas** de eventos y jugadores en SQLite.
- **Configuración validada:** si `settings.yml` tiene un error, se indica la ruta y el valor, y se conserva la configuración anterior.
- **Mensajes totalmente editables** en `messages.yml`.

## Comandos

| Comando | Para quién | Descripción |
|---|---|---|
| `/dtc start [duración]` | Admin | Inicia un evento |
| `/dtc stop` | Admin | Cancela el evento |
| `/dtc location` | Admin | Elige el bloque con una varita |
| `/dtc reload` | Admin | Recarga la configuración |
| `/dtc status` | Admin | Estado del evento |
| `/dtc rewards pending` / `retry <id>` | Admin | Revisa y reintenta recompensas |
| `/dtc top` | Jugadores | Ranking del evento activo |
| `/dtc history` / `stats` / `next` | Jugadores | Historial, estadísticas y próximo evento |

## Requisitos

- Paper 1.21.x con Java 21 o superior.
- Opcionales: PlaceholderAPI, FancyHolograms, DecentHolograms.
- No es compatible con Folia.

## Pruebas

Probado con pruebas unitarias y en un servidor Paper 1.21.11 real, con y sin los plugins opcionales. No se ha probado en Paper 26.x.

---

<sub>Parte de **[Akame Plugins](https://github.com/AkamePlugins)**.</sub>
