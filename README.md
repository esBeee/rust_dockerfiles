# Dockerfiles for rust

Docker images providing rust.

## `docker-compose.yml` example

```yml
version: '3'
services:
  app:
    image: esbeee/rust:1.20.0-nightly
    command: cargo run
    working_dir: /app
    volumes:
      - .:/app
      - cargo:/root/.cargo
    environment:
      - USER=esBeee
    ports:
      - 8000:8000
volumes:
  cargo:
```
