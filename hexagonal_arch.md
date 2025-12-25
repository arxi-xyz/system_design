# Hexagonal Architecture

## Shit notes 📓

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

## Adapter

**Adapter:** Adapter implements ports defined by the core (business logic). its like translator between inbound/outbound technology.You may have multiple adapters per port, including test adapters (fake/mock implementations).Ports are defined inside the core, adapters live outside and depend on those ports..

## Main Component

**Main Component:** Beside of these explanation we need a main component in this architecture. this component has this duty to runs at startup and build whole system by these instructions:

- initial configuration environment (Database, servers, mq and etc)
- Choose a driven(outbound) adaptors that implement ports and create instance for it.
- create application(hexagon) instance and inject driven adapters into it.
- for each driver port we create adapter and inject application instance for to it

## Refrences 📚

- [Ports And Adaptors](https://jmgarridopaz.github.io/content/hexagonalarchitecture.html) by  [jmgarridopaz](https://github.com/jmgarridopaz)

## Questions ❓

- which time do we need hexagonal arch? for which scenarios this arch is the best? what are the alternatives?
