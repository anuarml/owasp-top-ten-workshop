# The OWASP Top Ten Workshop

Workshop based on the [OWASP Top Ten](https://owasp.org/www-project-top-ten/) security vulnerabilities

## Requirements

- Node LTS
- docker
- docker-compose
- Postman for testing requests

|     Application                       |     Link                                              |     Notes                                                                                                                                                                                                                     |   |   |
|--------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|---|
|     Git                              |     https://git-scm.com/downloads                                               |     Configurar git con su cuenta https://docs.github.com/en/get-started/getting-started-with-git/set-up-git                                                                                                                   |   |   |
|     Github Desktop (opcional)        |     https://desktop.github.com/download/                                        |     Crear cuenta en github https://github.com/signup                                                                                                                                                                          |   |   |
|     Postman                          |     https://www.postman.com/downloads/                                          |     Crear cuenta de postman      https://identity.getpostman.com/signup                                                                                                                                                       |   |   |
|     NVM (opcional)                   |     https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating    |                                                                                                                                                                                                                               |   |   |
|     NodeJS (LTS)                     |     https://nodejs.org/en/download/prebuilt-installer/current                   |     Si instalaron nvm, usar nvm para   instalar NodeJS                                                                                                                                                                        |   |   |
|     NPM                              |     https://docs.npmjs.com/downloading-and-installing-node-js-and-npm           |     NPM usualmente viene instalado con   NodeJS así que no deberían de tener que instalarlo por separado, pero si por   alguna razón no lo tienen, favor de instalarlo.           Si tienen nvm usarlo para instalar   npm    |   |   |
|     Docker                           |     https://www.docker.com/get-started/                                         |     Crear cuenta en Docker https://app.docker.com/signup                                                                                                                                                                      |   |   |
|     Docker compose                   |     https://docs.docker.com/compose/install/                                    |                                                                                                                                                                                                                               |   |   |
|     Docker desktop (opcional)        |     https://docs.docker.com/desktop/                                            |     Dar click donde dice “install   Docker desktop” y seleccionar el sistema operativo                                                                                                                                        |   |   |
|     Git bash (opcional – Windows)    |     https://gitforwindows.org/                                                  |     Git bash debería instalarse cuando   instalen git pero si no, favor de instalarlo.           Nota: Solo aplica para windows                                                                                               |   |   |

### Postman instructions

1. Create  Postman account (if you don't have one)
2. Open Postman and login
3. Import the Postman collection from the `postman` folder (file -> import)

## Instrucciones para antes del taller

1.	Validar que se tengan instaladas todas las aplicaciones mencionadas en la tabla anterior con su respectiva configuración de cuentas.
2.	Clonar el repositorio del taller https://github.com/anuarml/owasp-top-ten-workshop/tree/master
    -	https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository
3.	Correr el “setup” del proyecto
    - En una terminal (si estas usando Windows de preferencia usar git bash) correr los siguientes comandos:
      1.	Ubicarse en la raiz del folder del repositorio clonado (cd <path>)
      2.	npm install 
      3.	npm run db:up (verificar que para este paso tengan Docker corriendo)
      4.	npm run db:migrate
4.	Validar que todo haya funcionado correctamente corriendo el siguiente comando
    - npm start (debería abrir una ventana en el navegador con una presentación)

## Setup

- `npm install`
- `npm run db:up`
- `npm run db:migrate`
- `npm run db:down` (**ONLY AFTER THE WORKSHOP IS FINISHED**)

## Slides

Slides contain instructions for the workshop.

`npm start` will open the slides in the browser

## Running an exercise

```bash
cd src/a01-access-control
npm start
```

## Verifying an exercise solution

This will run automated tests that fail until the issue in the exercise has been solved

(Some steps of the workshop might not have automated tests)

```bash
cd src/a01-access-control
npm run verify
```

## Run exercise verification tests on a single project

- `npm run verify -w src/a01-access-control`
