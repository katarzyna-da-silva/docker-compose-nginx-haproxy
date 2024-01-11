# Docker Compose Configuration - Version '3'

This Docker Compose file defines three services: HAProxy, nginx1, and nginx2. 

## Services:

### 1. HAProxy:

- Image: haproxy:latest
- Ports:
   - Host: 85
   - Container: 80
- Volume:
   - ./haproxy.cfg:/usr/local/etc/haproxy/haproxy.cfg

### 2. nginx1:

- Image: nginx:latest
- Ports:
   - Host: 8081
   - Container: 80

### 3. nginx2:

- Image: nginx:latest
- Ports:
   - Host: 8082
   - Container: 80

## Configuration for HAProxy:

 edit the `haproxy.cfg` file, which is mapped to the local volume `/usr/local/etc/haproxy/haproxy.cfg` in the HAProxy container. 

### Starting:

docker-compose up -d
