Annotator Store Dummy App
=========================

Rails app used to test the annotator-store Rails engine. This **wasn't intended
to be used in production**.


Database
--------

### Configuration & Creation

The database details are defined in the `config/database.yml`. At a minimum, on
your end the application expects a working Postgres database and a user with the
following credentials.

```
username: dummy
password: dummy_password
```

Make sure the user has permissions to create databases. It will handle the rest.

### Creation

First create the tables in the database by running `$ bin/rake db:create`. This
will create 3 tables for each environment:

* _dummy_astore_development_ - used when running the app in development mode.
* _dummy_astore_test_ - used by the app when running the specs/tests.
* _dummy_astore_production_ - used when running the app in production mode.

Then run the migration by running `$ bin/rake db:migrate` to create the database
structure i.e. columns, indices in the table for you.

Read more on [Active Record Migrations here][1].

[1]: http://guides.rubyonrails.org/migrations.html