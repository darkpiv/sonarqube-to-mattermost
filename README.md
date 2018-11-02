# sonarqube-2-slack
get information from Sonarqube then notif to slack channel

![demo image](images/demo.png)

# run with command

```
SONAR_USERNAME=temp SONAR_PASSWORD=abc12 SLACK_CHANNEL=#general PROJECT_ALIAS_NAME=gu_falcon1 SLACK_HOOK_URL=https://hooks.slack.com/services/ SONAR_URL=http://sonarqube.example.com/ go run sonar-2-slack.go
```

# run with docker. 
Docker images from [darkpiv/sonarqube-2-slack](https://hub.docker.com/r/darkpiv/sonarqube-2-slack)

```
docker pull darkpiv/sonarqube-2-slack
docker run --rm -e SONAR_USERNAME="temp"   \
-e SONAR_PASSWORD="abc123" \
-e SLACK_CHANNEL="#general" \
-e PROJECT_ALIAS_NAME="gu_falcon1" \
-e SLACK_HOOK_URL="https://hooks.slack.com/services" \
-e SONAR_URL="http://sonarqube.example.com/" darkpiv/sonarqube-2-slack
```


# Tasks

- [x] Read data from SonarQube
- [x] Design message send to slack
- [x] Push Message to slack
- [x] Dockersize app
- [ ] Handler fail case
- [ ] Write testcase
