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
