# Mailcow
## 1. Update
```bash
apt update 
apt upgrade -y
apt install curl git -y
```

## 2. Installation
### 2.1 install Docker
```bash
curl -sSL https://get.docker.com/ | CHANNEL=stable sh
systemctl enable --now docker
```


### 2.2 Mailcow

```bash
umask # <- Verify it is 0022
cd /opt
git clone https://github.com/mailcow/mailcow-dockerized
cd mailcow-dockerized
```

## 3. Initalize

```bash
./generate_config.sh
```

```bash
nano mailcow.conf
```

## 4. Run Mailcow
```bash
docker compose pull
docker compose up -d
```
