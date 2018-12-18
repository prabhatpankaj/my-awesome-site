# my-awesome-site

```
curl -sL https://raw.githubusercontent.com/prabhatpankaj/ubuntustarter/master/initial.sh | sh
```

```
sudo apt-get update \
  && sudo apt-get install -qy docker.io
  
sudo usermod -aG docker ${USER}
sudo service docker restart

```
* Running Jenkins Master
We use the latest Jenkins LTS image. Jenkins Web Dashboard is exposed on port 38080. Slave agents may connect master on default 50000 JNLP (Java Web Start) port.

```
docker run -d --name jenkins -p 38080:8080 -p 50000:50000 jenkins/jenkins:lts

```

* get initial password

```
docker logs jenkins

```
