## 1) Setup Ubuntu machine
```
1) Install docker, kind, kubectl (or use user-data for aws instance)
2) Create a kind cluster
3) Create a new user (give sudo privilages and set a ssh-key)
```

## 2) Add secrets for github actions
### Repository -> Settings -> Security -> Secrets and Variables -> Actions -> New Repository Secret ->
```
DOCKER_HUB_USERNAME
DOCKER_HUB_TOKEN
SERVER_HOST
SERVER_USER
SERVER_SSH_KEY
```
