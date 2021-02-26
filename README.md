# Sonarqube - Docker compose

Version included : `8.6.1`

That'll be pretty straightforward :

```bash
docker-compose up -d
```

Default port is 9000 and credentials are `admin`/`admin`

:information_source: The 8.7 version of SonarQube currently seem to have issues with Docker. It won't start.

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
