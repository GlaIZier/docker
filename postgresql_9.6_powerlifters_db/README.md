### To build container use command  
```
docker build -t official/postgresql:9.6 .
```

All init files are places in init_scripts folder

### To run docker container use command
```
docker run -d -v ~/github/docker_images/postgresql_9.6_powerlifters_db/init_scripts:/docker-entrypoint-initdb.d -p 8432:5432 --name postgres official/postgresql:9.6

```

### To connect to postgres from host machine use command
```
psql -h localhost  -p 8432 -U powerlifter -d powerliftersdb
```

### Or connect to docker container
```
docker exec -it postgres bash
```