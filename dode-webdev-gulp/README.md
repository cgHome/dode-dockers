# dode - gulp web-service development image 

Documentation: (https://github.com/cgHome/dode)

## Installation:

Add "scripts" entry within your service's `package.json` file:
```json
# Inside package.json...
{
  "scripts": {
    "start": "echo \"Error: no start specified\" && exit 1",
    "test": "echo \"Error: no test specified\" && exit 1",
    "lite": "lite-server"
  }
}
```
Scripts description:

+ npm start - runs the service start script
+ npm test - runs the service test scripts
+ npm run lite - runs the lite-server, a light-weight, static file server with excellent support for Angular apps that use routing

## Usage:

Run
```sh
docker run --rm \
    -v ./web:/home \  
    -p  8080:8080 \
    cghome/dode-webdev-gulp
```

Building this image
```sh
docker build -t cghome/dode-webdev-gulp .
```

Push
```sh
docker push cghome/dode-webdev-gulp 
```