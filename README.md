# django_postgres

### Run from the project directory
docker-compose run --rm app django-admin startproject app (This will create an 'app' directory and populate it.)

docker-compose build

### Initial db migration
docker-compose run --rm app python manage.py migrate

### Create super user
docker-compose run --rm app python manage.py createsuperuser

### Launch the containers
docker-compose up

### Launch the webpage
http://localhost:3003/admin

The user is 'appuser'.

The password is 'password'. (highly guessable)

### To access the db container:
'docker-compose ps' to get the name.

'docker exec -it "<name>" sh'

### To access the database:
'psql -U appuser test-db'
