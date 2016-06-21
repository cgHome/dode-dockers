# dode - (base) web-service development image

Documentation: (https://github.com/cgHome/dode)  

## Installation:

Add "scripts" entry within your service's `package.json` file:
```json
# Inside package.json...
{
  "scripts": {
    "start": "echo \"Error: no start specified\" && exit 1",
    "test": "echo \"Error: no test specified\" && exit 1"
  }
}
```
Scripts description:

+ npm start - runs the service start script
+ npm test - runs the service test scripts

## Usage:

Run
```sh
docker run --rm \
    -v ./web:/home \  
    -p  8080:8080 \
    cghome/dode-webdev
```
Building this image
```sh
docker build -t cghome/dode-webdev .
```
Push
```sh
docker push cghome/dode-webdev 
```