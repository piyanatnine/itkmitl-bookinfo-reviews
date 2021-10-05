# How to run reviews service

## How to run with Docker

```bash
# Build Docker Image for reviews service
docker build -t reviews .

# Run reviews service on port 8082
docker run -d --name reviews -p 8082:9080 \
--link ratings:ratings -e ENABLE_RATINGS=true -e "RATINGS_SERVICE=http://ratings:8080" reviews
```

* Test with path `/health` and `/reviews/1`