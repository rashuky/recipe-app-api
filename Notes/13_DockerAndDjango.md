# Using docker and django together

## Advantages
- Consistent dev and prod. env.
- easier collab.
- capture all dependencies as code
- easier cleanup 
- saves a LOT of time

## Drawbacks
- vscode unable to access interpreter
- more difficult to use integrated feature

Drawbacks are not that big. Terminal can be use instead.

## Configure docker
- Create a dockerfile
- Stepf for creating an image
    - Choose a base image (python)
    - install dependencies
    - Setup users (? Linux users needed to run our app)

## Docker compose
- how docker images should be use to run our dev. server
- define images as different services
    - name
    - map ports 
    - volume mappings (how our code get into a docker container)

## Using docker compose
- run all commands through Docker compose

Example 

`docker-compose run --rm app sh -c "python manage.py collectstatic"`

- --rm removes the container after run
- app name of the service
- sh -c passes in a shell command



