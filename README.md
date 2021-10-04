## Environment Variables

Use .env files to manage the environment variables.

## Routes Option

```
rails routes -h
```

## Setup

1. Checkout the app from version control
2. Make sure Postgres is running
3. Run `bin/setup`

## Running the App

1. `bin/run`

## Tests and CI

1. `bin/ci` runs the tests.
2. `tmp/test.log` will use the production logging format *not* the development one.

## Production

* All runtime configuration should be supplied in the UNIX environment
* Rails logging uses lograge. `bin/setup help` shows how to see this locally

## Issues

1. Database connection problem.

```
bparanj@localhost:~/play/rails/sustain/widgets$ bin/run
=> Booting Puma
=> Rails 6.1.4.1 application starting in development
=> Run `bin/rails server --help` for more startup options
Puma starting in single mode...
* Puma version: 5.5.0 (ruby 3.0.2-p107) ("Zawgyi")
*  Min threads: 5
*  Max threads: 5
*  Environment: development
*          PID: 2833203
* Listening on http://0.0.0.0:3000
Use Ctrl-C to stop
Started GET "/" for 127.0.0.1 at 2021-10-04 09:19:17 -0400

ActiveRecord::ConnectionNotEstablished (could not translate host name "db" to address: Temporary failure in name resolution
):
```
