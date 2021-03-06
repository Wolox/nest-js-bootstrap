# {{projectName}}

> {{projectDescription}}

---

## Pre-reqs โ๏ธ

<p align="center">
  <img src="https://img.shields.io/static/v1.svg?label=Node&message=v >= 16.16.0&labelColor=339933&color=757575&logoColor=FFFFFF&logo=node.js" alt="Node.js website"/>
  <img src="https://img.shields.io/static/v1.svg?label=Npm&message=v >= 8.11.0&labelColor=CB3837&logoColor=FFFFFF&color=757575&logo=npm" alt="Npm website"/>
  <img src="https://img.shields.io/static/v1.svg?label=Nest&message=v >=9.0.4&labelColor=444&logoColor=FFFFFF&color=757575&logo=NestJs" alt="NestJS website"/>
  <img src="https://img.shields.io/static/v1.svg?label=Typescript&message=v >= 4.7.4&labelColor=0678cc&logoColor=FFFFFF&color=757575&logo=Typescript" alt="Typescript website"/>
</p>

---

## Contents ๐ฆ

- [Installation](#installation-โ๏ธ)
- [Docker](#docker-๐ณ)
- [Running the app](#running-the-app-๐)
- [Test](#test-๐งช)
- [Linter](#linter-โ)
- [Debug config](#debug-config-๐ง)
- [API Docs](#api-docs-๐๏ธ)
- [Conventions](#conventions-๐ฉ)
- [Microservice status](#microservice-status-๐ข)

---

## Installation โ๏ธ

### 1. Clone repo

### 2. Entry

```shell
$ cd {{projectName}}
```

### 3. Install dependencies

```shell
$ npm install
```

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## Docker ๐ณ

For checking the containers status and some details just run:

```shell
$ sudo docker-compose ps -a
```

```bash
# Compose the docker containers
$ npm run docker:up

# To down the docker containers
$ npm run docker:down

# To debug
$ npm run docker:debug
```

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## Running the app ๐

```bash
# development mode
$ npm run start

# watch development mode (recommended)
$ npm run dev

# debug mode
$ npm run debug

# production mode
$ npm run start:prod
```

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## Test ๐งช

```bash
# unit/integration tests
$ npm run test

# test coverage
$ npm run coverage
```

<small>Note:<i>You can see the testing coverage report in the coverage folder.</i></small>

```bash
# Debug mode
$ npm run test:debug

# Watch mode
$ npm run test:watch
```

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## Linter โ

We use ESlint and Prettier.

```bash
# Lint and fix
$ npm run lint

# code format
$ npm run format
```

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## Debug config ๐ง

1. Add new file `./vscode/launch.json`

```json
{
  "configurations": [
    {
      "name": "Attach",
      "port": 9229,
      "request": "attach",
      "skipFiles": ["<node_internals>/**"],
      "type": "pwa-node"
    }
  ]
}
```

2. Define breakpoints

3. Run debug command

```shell
$ npm run debug
```

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## API Docs ๐๏ธ

### 1. Endpoints documentation

Swagger is a tool to design and document API's at scale. In this repo we use openapi v3.

Only enabled on develop and staging mode.

Start your app in local mode and visit: http://localhost:3000/api

### 2. Code documentation

Like NestJS, in this project we use Compodoc, a documentation tool for Angular. By documenting the code, members of the development team can easily understand the features of the application or library. Documentation is annotated using JSDoc.

#### 2.1 Generate documentation with:

```shell
$ npm run doc
```

#### 2.2 View documentation:

Visit: http://localhost:8080

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## Conventions ๐ฉ

View info:

- [Semantic versioning](https://semver.org/)
- [Conventional commits](https://www.conventionalcommits.org/en/v1.0.0-beta.4/)

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## Microservice status ๐ข

You can check the status of the microservice:

```curl
curl --location --request GET '{{service}}/api/health'
```

```curl
curl --location --request GET '{{service}}/api/version'
```

---

โช๏ธ - [Back](#contents-๐ฆ)

---

## Contributors ๐ท

- Yovanny Lรณpez (Backend Developer)

---

## Copyright ยฉ๏ธ

Copyright (C) {{year}}. All rights reserved.

License: {{license}}
