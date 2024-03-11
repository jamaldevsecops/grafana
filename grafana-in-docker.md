#### 1. Go to the directory where the dockerc-compose.yml file will be kept. 
```
mkdir grafana && cd grafana 
```
#### 2. Copy the following contents and past them in the docker-compose file.  

```
touch dockerc-compose.yml && vim dockerc-compose.yml
```

```
version: "3.9"
services:
  grafana:
    image: grafana/grafana
    container_name: grafana
    ports:
      - "3000:3000"
    volumes:
      - grafana_data:/var/lib/grafana
      - grafana_config:/etc/grafana
    restart: unless-stopped

volumes:
  grafana_data:
  grafana_config:
```
