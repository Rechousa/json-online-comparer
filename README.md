# Json Online Comparer

## Build docker image:

```
docker build -t rechousa/json-online-comparer:latest .
```

### Run:

1. Run the docker image:

```
docker run -it -p 8080:80 --rm --name json-online-comparer-1 rechousa/json-online-comparer:latest
```

2. Open a web browser and navigate to:
   http://localhost:8080/
