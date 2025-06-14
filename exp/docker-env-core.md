### > docker env

```
networks:
  backend:
  # mongo-network:
  #   driver: bridge

volumes:
  pg_data:
  minio_data:
  pgadmin_data:
  redis_data:
  redisinsight_data:
  mongodb_data:

services:
  # nestjs:
  #   image: nestjs
  #   build:
  #     context: self-up-be
  #     dockerfile: ./Dockerfile
  #   container_name: nestjs_app
  #   restart: always
  #   environment:
  #     NODE_ENV: production
  #     DATABASE_URL: postgres://postgres:admin@postgres:5432/self-up
  #     REDIS_HOST: redis
  #     REDIS_PORT: 6379
  #     S3_ENDPOINT: http://minio:9000
  #     S3_ACCESS_KEY: admin
  #     S3_SECRET_KEY: admin12345
  #     S3_BUCKET_NAME: my-bucket
  #   ports:
  #     - 3000:3000
  #   depends_on:
  #     - postgres
  #     - redis
  #     - minio

  # postgres:
  #   image: postgres:latest
  #   container_name: self-up-postgres
  #   restart: always
  #   environment:
  #     POSTGRES_USER: postgres
  #     POSTGRES_PASSWORD: admin
  #     POSTGRES_DB: self-up
  #   ports:
  #     - 5432:5432
  #   volumes:
  #     - pg_data:/var/lib/postgresql/data
  #   networks:
  #     - backend

  # pgadmin:
  #   image: dpage/pgadmin4:latest
  #   container_name: self-up-pgadmin
  #   restart: always
  #   environment:
  #     PGADMIN_DEFAULT_EMAIL: pgadmin4@pgadmin.org
  #     PGADMIN_DEFAULT_PASSWORD: admin
  #   ports:
  #     - "5050:80"
  #   # depends_on:
  #   #   - postgres
  #   volumes:
  #     - pgadmin_data:/var/lib/pgadmin
    # networks:
    #   - backend

  # mongodb:
  #   image: mongo:latest
  #   container_name: self-up-mongodb
  #   ports:
  #     - "27017:27017"
  #   volumes:
  #     - mongodb_data:/data/db
  #   environment:
  #     - MONGO_INITDB_ROOT_USERNAME=admin
  #     - MONGO_INITDB_ROOT_PASSWORD=password
  #   networks:
  #     - mongo-network
  #     - backend

  # mongo-express:
  #   image: mongo-express:latest
  #   container_name: self-up-mongo-express
  #   ports:
  #     - "8081:8081"
  #   environment:
  #     ME_CONFIG_MONGODB_ADMINUSERNAME: admin
  #     ME_CONFIG_MONGODB_ADMINPASSWORD: password
  #     ME_CONFIG_MONGODB_SERVER: mongodb
  #     # admin && pass
  #   depends_on:
  #     - mongodb
  #   networks:
  #     - mongo-network
  #     - backend

  # redis:
  #   image: redis:latest
  #   container_name: self-up-redis
  #   restart: always
  #   ports:
  #     - 6379:6379
  #   volumes:
  #     - redis_data:/data
  #   command: ["redis-server", "--appendonly", "yes"]
  #   networks:
  #     - backend

  # redisinsight:
  #   image: redislabs/redisinsight:latest
  #   container_name: self-up-redisinsight
  #   restart: always
  #   ports:
  #     - "5540:5540"
  #   depends_on:
  #     - redis
  #   volumes:
  #     - redisinsight_data:/db
  #   networks:
  #     - backend

  minio:
    image: minio/minio:latest
    container_name: self-up-minio
    restart: always
    ports:
      - "9009:9000"  # API S3
      - "9001:9001"  # MinIO Web UI
    environment:
      MINIO_ROOT_USER: admin
      MINIO_ROOT_PASSWORD: admin12345
    volumes:
      - minio_data:/data
    # networks:
    #   - backend
    command: server --console-address ":9001" /data
    

```
