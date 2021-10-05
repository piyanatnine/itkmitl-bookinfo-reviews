# How to run reviews service

## How to run with Docker

```bash
# Build Docker Image for reviews service
docker build -t reviews .

# Run reviews service on port 8082
docker run -d --name reviews -p 8082:9080 reviews
```

* Test with path `/health` and `/reviews/1`