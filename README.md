# Harness Lab App

A simple Java HTTP application for the Harness CI/CD. It serves:
- `GET /` — a greeting
- `GET /health` — health check response

## Local validation
```bash
mvn -B clean verify
java -jar target/harness-lab-1.0.0.jar
```
In another terminal:
```bash
curl http://localhost:8080/
curl http://localhost:8080/health
```

## Docker
```bash
mvn -B clean package
docker build -t harness-lab:local .
docker run --rm -p 8080:8080 harness-lab:local
```
