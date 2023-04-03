# dagster_poc

This is a [Dagster](https://dagster.io/) project that can be used as a template for data engineering @ RKI

## Getting started

This project is set up with make and poetry. To get started, run:

```bash
make install
```

Then, start the Dagster UI web server:

```bash
make dev
```

Open http://localhost:3000 with your browser to see the project.

You can start writing assets in `dagster_poc/assets.py`. The assets are automatically loaded into the Dagster code location as you define them.

## Development


### Adding new Python dependencies

You can add new Python dependencies in with poetry.

### Unit testing

Tests are in the `dagster_poc_tests` directory and you can run tests using `pytest`:

```bash
make test
```
to run unit tests once or 
```bash
make watch
```
to run unit tests on file changes.

### Schedules and sensors

If you want to enable Dagster [Schedules](https://docs.dagster.io/concepts/partitions-schedules-sensors/schedules) or [Sensors](https://docs.dagster.io/concepts/partitions-schedules-sensors/sensors) for your jobs, the [Dagster Daemon](https://docs.dagster.io/deployment/dagster-daemon) process must be running. This is done automatically when you run `dagster dev`.

Once your Dagster Daemon is running, you can start turning on schedules and sensors for your jobs.

## Deploy on Dagster on premise

This project is set up with a Jenkinsfile that can be used to deploy to a Dagster on premise instance. To use it, set up a Jenkins pipeline on your [Jenkins Instance](https://jenkins.tkpoc.it32.labor/).

[Contact your Dagster Administrator](mailto:kolbj@rki.de) to set up continous deployment of the image to our Dagster on premise deployment.
