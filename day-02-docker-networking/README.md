# Day 02: Docker Networking & Service Discovery



## Commands Executed



```bash

# Create custom bridge network

docker network create lab-network



# Run Nginx with Bind Mount

docker run -d --name web-server --network lab-network -v $(pwd)/html:/usr/share/nginx/html:ro nginx:alpine



# Test container resolution

docker run --rm --network lab-network curlimages/curl:latest curl -s http://web-serve
