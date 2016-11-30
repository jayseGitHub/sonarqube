# sonarqube

Docker container with sonar and sonar scanner. A simple way to test PHP project.
SonarQube is an open source platform for continuous inspection of code quality.

Version

Dependencies
Linux 4.4.0-47-generic amd64
Java 1.8.0_111 Oracle Corporation (64-bit)
SonarQube:latest 6.1
SonarQube Scanner 2.8 - Compatible with SonarQube 5.6+ (LTS)
http://docs.sonarqube.org/display/SCAN/Analyzing+with+SonarQube+Scanner
Php Plugin 2.9.1 - Compatible with SonarQube 5.6+ (LTS)
http://docs.sonarqube.org/display/PLUG/PHP+Plugin

Run SonarQube
The server is started this way:
$ docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 -v "$PWD":/root/src jayse/sonarqube
You can run a simple scanner :
$ docker exec -it sonarqube bash
$ bin/sonar-scanner -D sonar.projectKey=HelloWorld -D sonar.sources=/root/src/ -D sonar.projectBaseDir=/root/src/ -D sonar.language=php -D sonar.scm.disabled=true

This image is updated via pull requests to the GitHub repo https://github.com/jayseGitHub/sonarqube.

The Git repo of the image for SonarQube https://hub.docker.com/r/jayse/sonarqube/. See the Hub page for the full readme on how to use the Docker image.
