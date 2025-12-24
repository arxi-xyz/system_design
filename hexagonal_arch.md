# Hexagonal Architecture

## Shit notes 📓

- Adaptor: A technology-specific implementation of a port that translates between the external world and the core.

## Intro 📢

Hexagonal architecture aims for create sepration between core buisness logic and external services. This Architecture makes testing, maintaining and extending much easier. Hexagonal architecture promote decoupling from techonology and frameworks mindset also make sure you app stay independent of external services like framework database or tools.

## Structure 🏗️

Mainly hexagonal architecture maintain 3 parts yet. **Port, Hexagon, Adaptor**

### Hexagon

**Hexagon:** Means the core of application that contains rules and buisness logic. this part is completely independent (from framwork, database, webserver and etc.)

### Port

**Ports:** Interface defined by the application that describes how the core can be used or what it needs from outside. Ports has 2 type:

> Before Desrcibing the types you need to know driver and driven.
> **Driver** means where the flow of application starts for example http request, cli command or just a User
> **Driven** means where the interaction of application starts for example databases, caching layer or even external urls

- **inbound ports:** Inbound port is interface that describe the application usecases can give to driver.
- **outbound ports:** Outbound port is interface that describe what feature application expect from external systems

## Refrences 📚

- [Ports And Adaptors](https://jmgarridopaz.github.io/content/hexagonalarchitecture.html) by  [jmgarridopaz](https://github.com/jmgarridopaz)
