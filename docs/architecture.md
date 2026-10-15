# Architecture

## Current shape

```text
Browser
  |
  v
JSP views (index / tickets)
  |
  v
Ticket service -> JPA/Hibernate -> MySQL
                              ^
                              |
                    Flyway migration assets

Maven packages a WAR for Tomcat; Docker Compose models local MySQL, Flyway, and app services.
```

## Domain implementation

The application defines a ticket entity and status enum, a small ticket service, JSP pages, and a first Flyway migration with sample data. The codebase is a traditional servlet/JSP-style implementation rather than a modern Spring Boot or SPA architecture.

## Configuration boundary

Database credentials appear in tracked build, persistence, and container configuration. This is unsuitable for any shared or deployed environment. The documentation intentionally does not reproduce values; removal, rotation, and any history rewriting need a dedicated remediation task.

## Relationship to `xpeedopr`

The two repositories share a helpdesk domain but represent different technology approaches. `xpeedopr-java` is the legacy Java learning comparison; `xpeedopr` is the separate modern multi-stack demonstration.
