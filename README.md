## Movie Database UI (VueJS)

Tracker:
- [x] Connect to nodeRestApiServer endpoint
- [x] Created movie filters by loading movie data
- [x] Performed search operation and pass search criterias
- [x] Display movies information with pagination


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


### Running the application in Docker

You can run build and run the application from docker using the following commands:

**Build**

```shell script

> docker build -t redis/search-frontend  . 

```

This command will create a new image and build the maven project into it.

**Run**

```shell script
> docker run --rm  \
     --env "VUE_APP_SEARCH_API_JAVA=http://host.docker.internal:8085" \
     --env "VUE_APP_SEARCH_API_NODE=http://host.docker.internal:8086" \
     --env "VUE_APP_SEARCH_API_PYTHON=http://host.docker.internal:8087" \
     --name "redisearch-frontend"\
     -p 8084:8084 redis/search-frontend
```

Access the Web application with the following URL:

* http://localhost:8084
