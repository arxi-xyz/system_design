# hexagonal architecture

## Shit notes 📓

- Port and Adaptor
- aims for create sepration between core buisness logic and external services
- make easier to test - maintain and extend
- make sure you app stay independent of external services like framework database or tools
  me: but how?
- Hexagonal architecture promote decoupling from techonology and frameworks mindset
- Port: Interface defined by the application that describes how the core can be used or what it needs from outside.
- Adaptor: A technology-specific implementation of a port that translates between the external world and the core.
- Hexagon: The application core containing only business logic and rules, completely independent of external technologies.

## Structure 🏗️

Mainly hexagonal architecture maintain 3 parts yet. **Port, Hexagon, Adaptor**

### Hexagon

**Hexagon** Means the core of application that contains rules and buisness logic. this part is completely independent (from framwork, database, webserver and etc.)

### Port
