# mirakurun-chinachu-compose

- Mirakurun: https://github.com/Chinachu/Mirakurun
- Chinachu: https://github.com/aoirint/chinachu-docker

```shell
sudo apt install dvb-tools

git clone https://github.com/aoirint/mirakurun-chinachu-compose.git /opt/mirakurun-chinachu-compose
cd /opt/mirakurun-chinachu-compose

cp chinachu/conf/config.sample.json chinachu/conf/config.json

chown -R 1000:1000 chinachu/ mirakurun/

cp chinachu-docker-compose.service /etc/systemd/system/
cp mirakurun-docker-compose.service /etc/systemd/system/

systemctl enable mirakurun-docker-compose.service
systemctl restart mirakurun-docker-compose.service

systemctl enable chinachu-docker-compose.service
systemctl restart chinachu-docker-compose.service
```

## Notice

Based on <https://github.com/Chinachu/docker-mirakurun-chinachu> (MIT License).
