# NBIS webapp 
Docker setup for hosting NBIS web applications during development that require a password protection

The web applications should be provided as docker images, either existing in a repository or with a Dockerfile that can be built locally

## Setup 

### Create credentials
Create necessary login credentials in the `nginx` folder by the command `htpasswd`. For example, for the service `shiny-ortholog-seeker`, use the following command to create the password hash 


```
htpasswd -c nginx/.htpasswd-ortholog-seeker <username>
```

### Deploy 

The services can be deployed by

```
docker compose up -d
```

### Testing
There is a dummy Shiny application `app1` included in the setup. The hostname is `app1.nbiswebapp.bioshu.se` and 
login credentials are 
```
username: user1
password: pass1
```