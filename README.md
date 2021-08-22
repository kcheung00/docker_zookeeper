# Zookeeper Docker Image
This is zookeeper docker image based on minimal custom Ubuntu 20.04 docker image
- curl
- docker
- OpenJDK 11.0.11
- ssh
- wget

## Build Steps
1. Clone from git repo
   ```
   git clone https://github.com/kcheung00/docker_zookeeper.git
   ```
2. Build the image
   ```
   docker build -t my_zookeeper .
   ```
3. Exeecute the image in interactive mode
   ```
   docker run -it <Image ID> /bin/bash
   ```
4. Verify the image
   - Installed: wget, curl, ssh, docker, java
   - ./zkServer.sh [ start | status | stop ]
5. Tag the image
   ```
   docker tag <Image ID> kcheung00/my_zookeeper:3.4.13
   ```
6. Upload to docker hub
   ```
   docker push kcheung00/my_zookeeper:3.4.13
   ```