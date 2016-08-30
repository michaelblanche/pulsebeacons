# Pulse

### Deployment

To start development on your local machine just you use the following command:
```bash
bin/setup
```

For Ubuntu I recommend to execute to begin with:
```bash
./ubuntu.sh
```

It will take care of a few things:
- check Ruby version
- create `config/database.yml` database configuration file
  - ask which database adapter to use: Mysql/PostgreSQL
  - ask for database connection settings
- check Redis & Mysql/PostgreSQL client presence in the system and minimum required version
- create `config/config.yml` application configuration file
  - ask for Redis connection settings
  - ask for mailer URLs settings
  - ask for mailer SMTP settings
  - ask which extensions should be autoloadable
- create `config/sidekiq.yml` Sidekiq configuration file
- run `bundle install`
- verify connection to Redis and Mysql/PostgreSQL server
- create empty database and run migrations
- seed database with initial data
- create admin account and send confirmation email
- start application
