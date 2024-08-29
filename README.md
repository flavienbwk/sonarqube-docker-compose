# Sonarqube - Docker compose

Default version included : `10.6.0`

That'll be pretty straightforward :

```bash
sudo sysctl -w vm.max_map_count=512000
# Persist this setting in `/etc/sysctl.conf` and execute `sysctl -p`

cp .env.example .env
docker-compose up -d
```

Default port is 9000 and credentials are `admin`/`admin`

## Running sonar-scanner

We are going to scan some Python code in `./example/python_code`

1. First, go to the SonarQube interface, create a new project and grab :

   - The project key (you provide)
   - The SonarQube token (provided to you)

2. Configure them in `./example/.env`

3. Let's run our test :

    ```bash
    cd example
    docker-compose up
    ```

## Popular plugins for Community Edition

- Multi-branch : https://github.com/mc1arke/sonarqube-community-branch-plugin
- Active Directory SSO : https://github.com/hkamel/sonar-auth-aad
