## ALlCare Jenkins

For robust and maintainable usage of jenkins in AllcareSquad Team's CI/CD.

### Run

```
docker compose -f "docker-compose.yaml" up -d --build
```

### Data directory
- jenkins-data
- jenkins-docker-certs


### Excluded Sub-directories
 Due to sensitive data. See [.gitignore](https://github.com/AllCareSquad/allcare-jenkins/blob/main/.gitignore)

 ### Troubleshoot and Migration in Google Compute Engine
 Due to this repository is clean and please keeping it clean. Meaning that do not push any sensitive data or configurations.
 Make sure in the VM where is jenkins up and running:
 - stop the container first
 - rename existing directory jenkins-data to jenkins-data-old
 - then clone this repository
 - copy every sub directories inside jenkins-data-old which is listed in [.gitignore](https://github.com/AllCareSquad/allcare-jenkins/blob/main/.gitignore) to jenkins-data
 - run the docker compose
 - see the result