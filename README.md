Workarea Demo
================================================================================

Get a demo instance of Workarea running with Docker.

Setup
--------------------------------------------------------------------------------

To setup a demo application, you can run the following command:

```bash
curl -s https://raw.githubusercontent.com/workarea-commerce/workarea-demo/master/bin/install | bash
```

This will run a script that does the following:

* clone this repository.
* build a Docker image for the application
* start containers for the application and required services
* seed the database
* start the application server

Once complete, you can visit `http://localhost:3000` to view your app. The seed data provides an admin user with an email/password of `user@workarea.com/W3bl1nc!`.

To stop the application, run:

```bash
docker-compose down
```

If you want to restart an existing demo app, navigate to the `workarea-demo/` directory and run:

```bash
docker-compose up
```

Troubleshooting
--------------------------------------------------------------------------------

If any of the Docker containers fail to start make sure you do not have any other services or containers running that are using the same ports.

Workarea services use ports `27018`, `9201`, `6389`, and `3000`.

If `https://localhost:3000` seems sluggish, or completely unresponsive, you might need to increase Docker's memory allocation. We suggest at least 4GB.
