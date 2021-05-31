# dockerproject


Write to the Host Filesystem - docker volume
======================

    >  docker volume create docker-data
    docker-data
    >  docker volume ls
    DRIVER              VOLUME NAME
    local               docker-data
    > docker run -d--name devtest --mount source=docker-data,target=/app ubuntu:latest


Configure Logging
======================
    > docker run -it --log-driver json-file --log-opt mode=non-blocking ubuntu
    
    
Port Mapping
======================
    > docker port foo
      7000/tcp -> 0.0.0.0:2000
      9000/tcp -> 0.0.0.0:3000

    > docker run -p 127.0.0.1:80:9999/tcp ubuntu bash
    
          
Configure CPU
======================
    > docker run -it --cpus=".25" ubuntu /bin/bash
