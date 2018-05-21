---
layout: page
homepage: true
isHome: true
title: Astronomer Enterprise Edition
permalink: /
order: 1
---

# Overview

Astronomer Enterprise Edition is an enterprise-grade data
engineering platform that allows any developer to jump to the task
of creating and managing data pipelines very quickly. The platform
includes a Heroku-like CLI capability to deploy pipelines, as
well as a New Relic-like interface to monitor and troubleshoot
running pipelines.

The platform leverages leading open source tools
including Kubernetes, Airflow, Prometheus, and Grafana — and also
includes a library of
[open-source Airflow connectors](https://github.com/airflow-plugins)
that we have been building and curating for the past year.

<iframe width="560" height="315" style="display: block; margin: 4rem auto;"
  src="https://www.youtube.com/embed/J-qIzADJlV8"
  frameborder="0" allow="autoplay; encrypted-media"
allowfullscreen></iframe>

## Architecture

We’ve build out pre-configured Docker containers w/ Celery and metrics/monitoring.
The Astronomer Airflow module consists of seven components, and you must bring
your own Postgres and Redis database.

![Airflow Module]({{ "/assets/img/airflow_module.png" | absolute_url }})

This kit is fully open-sourced (Apache 2.0) and you can experiment with it at
[https://open.astronomer.io/airflow/](https://open.astronomer.io/airflow/).

## DAG Deployment

Astronomer Enterprise makes it easy to deploy these containers
to Kubernetes - but more importantly, to give Airflow developers a
CLI to deploy DAGs through a private Docker registry that interacts
with the Kubernetes API.

Components that glue this all together include
[Phoenix](https://github.com/astronomerio/phoenix) and
[Commander](https://github.com/astronomerio/commander).

![Airflow Deployment]({{ "/assets/img/airflow_deployment.png" | absolute_url }})

Remember to run `astro airflow init` after creating a new project directory.

Any Python packages can be added to `requirements.txt` and all OS level packages can be added to `packages.txt` in the project directory.

Additional [RUN](https://docs.docker.com/engine/reference/builder/#run
) commands can be added to the `Dockerfile`. Environment varaibles can also be added to [ENV](https://docs.docker.com/engine/reference/builder/#env).

## Astronomer CLI

The [Astronomer CLI](https://github.com/astronomerio/astro-cli) is
under very active development to
[support Airflow-related commands](https://github.com/astronomerio/astro-cli/blob/master/cmd/airflow.go).

## Airflow CLI

We’ll also make it easy to use the Airflow CLI remotely
(i.e. run commands from your local terminal that execute in the
cloud Airflow).

## Other community contributions

We’re building out a
[library of Airflow Plugins](https://github.com/airflow-plugins)
and we’re also doing an
[Airflow podcast](soundcloud.com/the-airflow-podcast).

## Building the Documentation

Documentation is built on Jekyll and hosted on Google Cloud Storage.

Build the docs site locally:

```
cd docs
bundle install
```

Run it:

```
bundle exec jekyll serve
```
