## Xmrig NVIDIA cryptonight (default) or cryptonight-lite
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

#### Simpleco.in - Default
```
nvidia-docker run -ti --rm --name Xmrig-nvidia-doge \
-e ALGORITHM="cryptonight" \
-e POOL="simpleco.in" \
-e PORT="8081" \
-e USER="luvres.7873" \
-e USERPASS="x" \
izone/xmrig-nvidia 
```

#### Nicehash (cryptonight)
```
nvidia-docker run -ti --rm --name Xmrig-nvidia-nicehash \
-e ALGORITHM="cryptonight" \
-e POOL="cryptonight.eu.nicehash.com" \
-e PORT="3355" \
-e USER="3PThBqHfb1UVcZaZXtPAY4SC4fZNBNqCs7.1uvr3z" \
-e USERPASS="x" \
izone/xmrig-nvidia 
```

#### Minergate XMR
```
nvidia-docker run -ti --rm --name Xmrig-nvidia-Minergate \
-e ALGORITHM="cryptonight" \
-e POOL="xmr.pool.minergate.com" \
-e PORT="45700" \
-e USER="1uvr3z@gmail.com" \
-e USERPASS="x" \
izone/xmrig-nvidia 
```

#### BBS Coin
```
nvidia-docker run -ti --rm --name Xmrig-nvidia-bbs \
-e ALGORITHM="cryptonight" \
-e POOL="78.46.85.142" \
-e PORT="19931" \
-e USER="fyTZ7jLeycCEYMpexDcUMCaxiErw7mFJDNMAJNShyWRA1dnf7ZmHgj8Zwd61VKiEjHDd8TsgZJL9h4ZdbYBdfCHv32d62EsgX" \
-e USERPASS="x" \
izone/xmrig-nvidia 
```

#### QWC Qwerty coin
```
nvidia-docker run -ti --rm --name Xmrig-nvidia-qwc \
-e ALGORITHM="cryptonight" \
-e POOL="78.46.85.142" \
-e PORT="8261" \
-e USER="QWC1GWTaTdNCGBnQPspUYZi3WUty9mDJPgCM3ohTupC1NjhL1uTzHed2xC3VV79P57A3L5ZWrzKC8a4hXifqwuyd4yQSrY82EK" \
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

