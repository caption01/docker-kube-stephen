### Docker Command Useful

//allow you to exec your command into container
docker exec -it (container) (command)

- bash, powershell, zsh, sh => command processor

//start up + exec command
docker run -it (container) (command)

- docker run -it busybox sh
