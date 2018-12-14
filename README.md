# Angular Jenkins CI

## This project is based upon [jenkinsci/docker](https://github.com/jenkinsci/docker)

## This project adds a docker-compose file for jenkinsci and comes preinstalled with xvfb + chrome drivers for headless testing!

### The reason behind this personal project was that my team needed headless E2E testing with xvfb + chrome driver preinstalled in the container

The Jenkins Continuous Integration and Delivery server [available on Docker Hub](https://hub.docker.com/r/adamino/angular-jenkinsci).

This is a fully functional Jenkins server.
[https://jenkins.io/](https://jenkins.io/).

<img src="https://jenkins.io/sites/default/files/jenkins_logo.png"/>


# Usage

First time the compose is done, I recommend running

```
docker compose-up
```

This way you will see the output of the container, which is needed because of the intial admin installation token ([read more(https://jenkins.io/doc/book/installing/)])

After initial installation, simply run

```
docker-compose up -d
```

