# Documentation
This is my [personal website](https://havluj.eu). I used the [Compass](https://github.com/excentris/compass) template as a starting point.

## How to run locally
Use Docker to run locally. 

Create docker-compose.yml at the root of your project:

```
version: '3'
services:
  jekyll:
    image: starefossen/github-pages
    environment:
      - "JEKYLL_GITHUB_TOKEN:${JEKYLL_GITHUB_TOKEN}"
    ports:
      - "4000:4000"
    volumes:
      - ./:/usr/src/app
    tty: true
```

Then start the container with `docker-compose up`.
