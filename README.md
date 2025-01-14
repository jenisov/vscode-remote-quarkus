# Vscode Remote Development Containers: [Quarkus](https://quarkus.io)

## dev mode

```bash
mvn clean compile quarkus:dev
```

call endpoint with `curl localhost:8080/hello`

## test

```bash
mvn clean test
```

## build native executable

```bash
mvn clean package -Pnative
# Find executable in `target` directory.
ls -l target
```

## run integration tests against native executable

```bash
mvn verify -Pnative
```

## build docker image with native executable

```bash
docker build -t quarkus/getting-started .
```

## run docker image with native executable

```bash
docker run --name getting-started -d -p 8081:8080 quarkus/getting-started
```
