Build the app
    docker compose build

Run the app
    docker compose up -d

List the containers
    docker compose ps

Look at the db container logs
    docker compose logs -f web-fe

COMPAS V2 Commands

LS will lis the current projects
    docker compose ls

Deploy a second version using a different project name
    docker compose -p test up -d

Cleanup
    docker compose down
    docker compose ls
    docker compose -p test down
    