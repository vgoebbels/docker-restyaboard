Docker Restyaboard
==============================

Build Restyaboard in Docker.

* Restyaboard  
  http://restya.com/board/

* Docker  
  https://www.docker.com/


Quick Start
------------------------------

Build image and Run container using docker-compose.

``` bash
git clone https://github.com/namikingsoft/docker-restyaboard.git
cd docker-restyaboard

COMPOSE_API_VERSION=1.18 docker-compose up -d
```


Include provisioning in AWS EC2
------------------------------

```bash
git clone https://github.com/namikingsoft/docker-restyaboard.git
cd docker-restyaboard

bundle install

cp .env.sample .env
vim .env

vagrant plugin install vagrant-aws
vagrant plugin install dotenv

vagrant up && bundle exec rake
```


Check URL
------------------------------

```
http://(ServerIP):1234
```


Other Command
------------------------------

#### Rake provisioning

```bash
bundle exec rake provision
```

#### Rake serverspec 

```bash
bundle exec rake spec
```

License
------------------------------

[OSL 3.0](LICENSE.txt)  
It fits in Restyaboard.
