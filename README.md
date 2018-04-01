## Xmrig
-----

### NVIDIA Docker (https://github.com/NVIDIA/nvidia-docker)
```
# Install nvidia-docker and nvidia-docker-plugin
wget -P /tmp https://github.com/NVIDIA/nvidia-docker/releases/download/v1.0.1/nvidia-docker_1.0.1_amd64.tar.xz
sudo tar --strip-components=1 -C /usr/bin -xvf /tmp/nvidia-docker*.tar.xz && rm /tmp/nvidia-docker*.tar.xz

# Run nvidia-docker-plugin
sudo -b nohup nvidia-docker-plugin > /tmp/nvidia-docker.log

# Test nvidia-smi
nvidia-docker run --rm nvidia/cuda nvidia-smi
```
-----

### Run

#### Simpleco.in
```
nvidia-docker run -ti --rm --name Xmrig-nvidia-simpleco.in \
-e ALGORITHM="cryptonight" \
-e POOL="simpleco.in" \
-e PORT="8081" \
-e USER="luvres.7873" \
-e USERPASS="x" \
izone/xmrig-nvidia 
```

-----
#### Build
```
docker build -t izone/xmrig-nvidia .
```
```
docker build -t izone/xmrig-nvidia:build -f Dockerfile_build .
```

