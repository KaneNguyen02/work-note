```
services:
  elasticsearch:
    image: docker.elastic.co/elasticsearch/elasticsearch:8.13.1
    container_name: elasticsearch
    environment:
      - discovery.type=single-node
      - xpack.security.enabled=false
      - "ES_JAVA_OPTS=-Xms512m -Xmx512m"
    volumes:
      - es-data:/usr/share/elasticsearch/data
    ports:
      - 9200:9200
    networks:
      - elastic
  
  kibana:
    image: docker.elastic.co/kibana/kibana:8.13.1
    container_name: kibana
    environment:
      - ELASTICSEARCH_HOSTS=http://elasticsearch:9200
    ports:
      - 5601:5601
    depends_on:
      - elasticsearch
    networks:
      - elastic

networks:
  elastic:
    driver: bridge

volumes:
  es-data:
```
