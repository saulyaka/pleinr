# Tatle: Pleinr / Repository: https://bitbucket.org/saulyaka/pleinr-django/src/develop/

# Author: Alla Popova
# Framework: Django
# Data base: PostgreSQL
# Project status: working/dev

# content db.env:
    POSTGRES_DB=postgres
    POSTGRES_USER=postgres
    POSTGRES_PASSWORD=postgres

# content dev.env:
    SECRET_KEY='some key'
    DJANGO_ALLOWED_HOSTS=localhost 127.0.0.1 [::1]

    SQL_ENGINE=django.db.backends.postgresql
    SQL_DATABASE=postgres
    SQL_USER=postgres
    SQL_PASSWORD=postgres
    SQL_HOST=db
    SQL_PORT=5432

    DEBUG=1
    HASHID_FIELD_SALT='Live is great on Tenerife'

# Useful commands:
python manage.py loaddata fixtures
> Load objects from fixtures.json. Replace objects if pk is matched.