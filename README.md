# CocaColita

Bot de integración entre **Minecraft 1.12.2** y **Discord** mediante **Mc2Discord**, utilizado por el servidor **CocaColita**.

Permite mantener a la comunidad informada en tiempo real sobre todo lo que ocurre dentro del servidor.

---

# Características

- 💬 Chat de Minecraft ↔ Discord
- 📥 Avisos de entrada y salida de jugadores
- 💀 Mensajes de muerte
- 🏆 Logros y avances
- 🟢 Inicio y apagado del servidor
- 📊 Estado de jugadores conectados
- 🖼️ Avatar de jugadores mediante mc-heads
- ⚙️ Configuración totalmente personalizable mediante TOML

---

# Requisitos

- Minecraft **1.12.2**
- Forge
- Java 8
- Discord Server
- Bot de Discord

---

# Instalación

## 1. Instalar el mod

Copiar:

```
mc2discord-forge-1.12.2-3.3.2.jar
```

dentro de:

```
/mods
```

---

## 2. Configuración

Editar:

```
config/mc2discord.toml
```

---

## 3. Crear un Bot de Discord

Crear una aplicación en:

https://discord.com/developers/applications

Activar los permisos necesarios y obtener el Token.

Introducirlo en:

```toml
token = "TU_TOKEN"
```

> **IMPORTANTE**
>
> Nunca publiques tu Token en GitHub ni lo compartas con otras personas.

---

# Configuración de Canales

Cada canal puede suscribirse a distintos eventos.

## Chat

```toml
subscriptions = ["chat"]
```

Recibe únicamente el chat de Minecraft.

---

## Información

```toml
subscriptions = ["info"]
```

Recibe:

- Inicio del servidor
- Apagado
- Jugadores conectándose
- Jugadores saliendo
- Muertes
- Avances

---

## Log

```toml
subscriptions = ["log"]
```

Recibe el registro del servidor.

---

# Mensajes personalizados

Todos los mensajes pueden modificarse.

Ejemplo:

```toml
join = "📥 ${player_display_name} se ha unido"
```

```toml
leave = "📤 ${player_display_name} ha salido"
```

```toml
death = "💀 ${death_message}"
```

```toml
advancement = "🏆 ${player_display_name} ha conseguido ${advancement_title}"
```

---

# Estado del Bot

El bot actualiza automáticamente su presencia.

Ejemplo:

```
5 jugadores conectados
```

También puede modificar automáticamente el nombre de un canal de Discord para mostrar:

```
📲┃Conectados 5
```

---

# Formato del chat

Discord → Minecraft

```
<Discord - Usuario> Hola
```

Minecraft → Discord

```
Jugador: Hola
```

---

# Avatar de jugadores

Configurado mediante:

```
https://mc-heads.net
```

Cada mensaje utiliza automáticamente la cabeza del jugador correspondiente.

---

# Comando /discord

Dentro del servidor los jugadores pueden utilizar:

```
/discord
```

para obtener la invitación del servidor.

---

# Archivos incluidos

```
mods/
└── mc2discord-forge-1.12.2-3.3.2.jar

config/
└── mc2discord.toml

privacy.html
terms.html
README.md
```

---

# Política de Privacidad

El proyecto incluye:

```
privacy.html
```

Documento que describe:

- Datos recopilados
- Uso de la información
- Conservación
- Seguridad
- Derechos de los usuarios

---

# Condiciones del Servicio

El proyecto incluye:

```
terms.html
```

Documento con:

- Normas de uso
- Responsabilidades
- Disponibilidad
- Propiedad intelectual
- Cambios en el servicio

---

# Tecnologías

- Minecraft Forge 1.12.2
- Mc2Discord
- Discord API
- TOML
- HTML5
- CSS3

---

# Licencia

Este proyecto está destinado al servidor **CocaColita**.

Puedes modificar la configuración para adaptarla a tu propio servidor.

---
