# dode - typescript web-service development image 

Documentation: (https://github.com/cgHome/dode)  

## Installation:

Included a number of npm scripts in the suggested ./web/package.json file to handle common development tasks:
```json
{
  "scripts": {
    "start": "tsc && concurrently \"npm run tsc:w\" \"npm run lite\" ",
    "test": "echo \"Error: no test specified\" && exit 1",
    "tsc": "tsc",
    "tsc:w": "tsc -w",
    "typings": "typings",
    "lite": "lite-server",
    "postinstall": "typings install",
  }
}
```

Scripts description:
+ npm start - runs the compiler and a server at the same time, both in "watch mode"

+ npm test - runs the service test scripts

+ npm run tsc - runs the TypeScript compiler once

+ npm run tsc:w - runs the TypeScript compiler in watch mode; the process keeps running, awaiting changes to TypeScript files and recompiling when it sees them

+ npm run lite - runs the lite-server, a light-weight, static file server with excellent support for Angular apps that use routing

+ npm run typings - runs the typings tool separately

+ npm run postinstall - called by npm automatically after it successfully completes package installation. This script installs the TypeScript definition files defined in typings.json

## Usage:
Run
```sh
docker run --rm \
    -v ./web:/home \  
    -p  8080:8080 \
    cghome/dode-webdev-tcs
```
Building this image
```sh
docker build -t cghome/dode-webdev-gulp .
```
Push
```sh
docker push cghome/dode-webdev-gulp 
```