# Adding new database

After adding new database to envs run:

```sh
docker exec -it postgres-postgres-1 bash /docker-entrypoint-initdb.d/01-init-databases.sh
```

This script is executed automatically on container start only if the data volume is empty
