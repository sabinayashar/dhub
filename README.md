# dhub
Task: Automate the deployment of an application to a containers/image registry. As an Automation Tool, use CircleCI, keep your sources in a GitHub public repo, and deploy to DockerHub.

How did I automate the deployment?
1. created identically named repositories in github and dockerhub
2. created .circleci/config.yml folder in the project and filled in with required information (eg. docker_user, docker_pass, dimage)
3. added jib-maven-plugin to pom.xml
4. binded circleci with github account
5. pushed the project to github
6. added environment variables to "dhub" project settings in circleci and reran workflow from start

How to run the app?
docker run -p 8080:8080 sabinayashar/dhub:latest
