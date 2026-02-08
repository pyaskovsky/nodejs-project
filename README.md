<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">A progressive <a href="http://nodejs.org" target="_blank">Node.js</a> framework for building efficient and scalable server-side applications.</p>
    <p align="center">
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
<a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/dm/@nestjs/common.svg" alt="NPM Downloads" /></a>
<a href="https://circleci.com/gh/nestjs/nest" target="_blank"><img src="https://img.shields.io/circleci/build/github/nestjs/nest/master" alt="CircleCI" /></a>
<a href="https://discord.gg/G7Qnnhy" target="_blank"><img src="https://img.shields.io/badge/discord-online-brightgreen.svg" alt="Discord"/></a>
<a href="https://opencollective.com/nest#backer" target="_blank"><img src="https://opencollective.com/nest/backers/badge.svg" alt="Backers on Open Collective" /></a>
<a href="https://opencollective.com/nest#sponsor" target="_blank"><img src="https://opencollective.com/nest/sponsors/badge.svg" alt="Sponsors on Open Collective" /></a>
  <a href="https://paypal.me/kamilmysliwiec" target="_blank"><img src="https://img.shields.io/badge/Donate-PayPal-ff3f59.svg" alt="Donate us"/></a>
    <a href="https://opencollective.com/nest#sponsor"  target="_blank"><img src="https://img.shields.io/badge/Support%20us-Open%20Collective-41B883.svg" alt="Support us"></a>
  <a href="https://twitter.com/nestframework" target="_blank"><img src="https://img.shields.io/twitter/follow/nestframework.svg?style=social&label=Follow" alt="Follow us on Twitter"></a>
</p>
  <!--[![Backers on Open Collective](https://opencollective.com/nest/backers/badge.svg)](https://opencollective.com/nest#backer)
  [![Sponsors on Open Collective](https://opencollective.com/nest/sponsors/badge.svg)](https://opencollective.com/nest#sponsor)-->

# NestJS Application

## Architectural Vision

### Project Overview

This project is built on the **NestJS framework** - a progressive Node.js framework that uses TypeScript for building efficient and scalable server-side applications. The project architecture is based on principles of **modularity**, **dependency injection**, and **clean architecture**.

### Application Structure

```
src/
├── app.module.ts          # Root application module
├── app.controller.ts      # Main controller
├── app.service.ts         # Main service
├── main.ts               # Application entry point
└── users/                # Users module
    ├── users.module.ts   # Users module
    ├── users.controller.ts # Users controller
    ├── users.service.ts  # Users service
    └── *.spec.ts         # Tests
```

### Architectural Principles

#### 1. Modular Architecture
The project is organized with a modular approach where each module is responsible for a specific domain:
- **AppModule** - root module that configures the application
- **UsersModule** - module for user management
- Future modules will follow the same pattern

#### 2. Separation of Concerns
- **Controllers** - handle HTTP requests, validate input data
- **Services** - business logic, data operations
- **Modules** - organize and wire components together

#### 3. Dependency Injection
NestJS provides automatic dependency injection, simplifying testing and code maintenance.

### Environment Configuration

The project uses a flexible environment configuration system:

#### Configuration File Hierarchy:
1. **.env.local** - local development settings (has priority)
2. **.env** - base application settings

#### Supported Environment Variables:
- `NODE_ENV` - environment (development/production)
- `PORT` - server port
- `DB_*` - database connection parameters
- `JWT_*` - JWT authentication settings
- `API_*` - API settings

### Why This Architecture?

#### Benefits of the Chosen Architecture:

1. **Scalability** - modular structure allows easy addition of new features
2. **Testability** - separation of concerns simplifies unit and integration tests
3. **Maintainability** - clear structure and TypeScript provide better code support
4. **Security** - configuration through environment variables protects sensitive data
5. **Performance** - NestJS is optimized for high-load applications

#### Technology Stack:
- **NestJS** - main framework
- **TypeScript** - typing and improved development
- **Express** - HTTP server (under NestJS hood)
- **Jest** - testing
- **ESLint + Prettier** - code styling

### Future Expansion

The architecture is ready for expansion:
- Adding new modules (Auth, Products, Orders, etc.)
- Database integration (PostgreSQL, MongoDB)
- Microservices architecture implementation
- WebSocket support
- External API integration

## Installation and Running

```bash
# Install dependencies
$ npm install

# Run in development mode
$ npm run start:dev

# Run in production mode
$ npm run start:prod

# Run tests
$ npm run test
```

## License

MIT Licensed
