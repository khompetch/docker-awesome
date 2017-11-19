

Getting started for Docker Engine CE (Free Version)
---------------------------------------------------

```
sudo mkdir -p /build && cd /build

sudo apt-get install git -y && sudo git clone https://github.com/drivesoft-technology/docker-awesome.git

cd /build/docker-awesome
```


Install Docker Engine CE v17.09.0 (Free Version)
---------------------------------------------------

```
bash /build/docker-awesome/docker-install/install-docker-engine-on-ubuntu16.sh
```


Install Docker Compose v1.17.0
---------------------------------------------------

```
bash /build/docker-awesome/docker-install/install-docker-compose-on-ubuntu16.sh
```


Build Phalcon3 PHP Mobule.
---------------------------------------------------

```
docker build -t build/php7phalcon:7.1.11 .
```


```
docker run -it --name docker-php7phalcon -d build/php7phalcon:7.1.11
docker cp docker-php7phalcon:/usr/local/etc/php/conf.d/20-phalcon.ini ./php7-ini/20-phalcon.ini
docker cp docker-php7phalcon:/usr/local/lib/php/extensions/no-debug-non-zts-20160303/phalcon.so ./php7-ext/phalcon.so
```


```
docker stop docker-php7phalcon && docker rm docker-php7phalcon
```