# 💬 ChatWave: Chat en tiempo real

Aplicación de mensajería en tiempo real con salas y mensajes privados.

> **Estado:** 🚧 en desarrollo

## Funcionalidades previstas

- [ ] Registro y login con JWT
- [ ] Salas públicas y mensajes privados
- [ ] Comunicación en tiempo real mediante WebSockets (STOMP)
- [ ] Indicador de presencia (conectado/desconectado)
- [ ] Indicador de "escribiendo..."
- [ ] Historial de mensajes persistido
- [ ] Reconexión automática del cliente
- [ ] Tests de concurrencia con múltiples clientes simultáneos

## Stack

| Capa | Tecnología |
|------|-----------|
| Backend | Java 21, Spring Boot 3, Spring WebSocket |
| Persistencia | Spring Data JPA, PostgreSQL |
| Frontend | [React / HTML + JS: por decidir] |
| Tests | JUnit 5 |
| DevOps | Docker |

## Estructura del proyecto

```
ChatWave/
├── backend/
│   ├── src/main/java/com/chatwave/
│   │   ├── config/        # Configuración (WebSocket, seguridad, CORS)
│   │   ├── controller/    # Endpoints REST y controladores STOMP
│   │   ├── dto/           # Objetos de transferencia de datos
│   │   ├── model/         # Entidades JPA
│   │   ├── repository/    # Repositorios Spring Data
│   │   ├── security/      # JWT y filtros de autenticación
│   │   ├── service/       # Lógica de negocio
│   │   └── websocket/     # Listeners de eventos (presencia, conexión)
│   ├── src/main/resources/
│   └── src/test/java/com/chatwave/
├── frontend/
├── docker/
└── docs/
```

## Cómo ejecutarlo

> Pendiente: se completará cuando exista la primera versión ejecutable.

```bash
git clone https://github.com/Panchitis311/ChatWave.git
cd chatwave
docker compose up
```

## Hoja de ruta

1. **Fase 1:** autenticación y chat básico entre dos clientes
2. **Fase 2:** salas, mensajes privados y persistencia
3. **Fase 3:** presencia, reconexión y pruebas de carga

## Licencia

MIT
