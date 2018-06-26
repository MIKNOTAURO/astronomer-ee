---
layout: page
title: RBAC
permalink: /guides/rbac/
hide: true
---

# Role based access control (RBAC)

## Terms

### Users

An OAuth-linked object that represents a human who has authenticated with the
Astronomer deployment.

### Deployments

A named Airflow cluster that is owned by an individual or team.

### Roles

A high-level, named bundle of policies and permissions that is used
to define a user's access to a team and group of deployments, i.e.
`owner`, `admin`, `user`. These are customizable for each Astronomer deployment
as global options, and also definable on a team basis.

### Teams

Teams contain a group of Airflow Cluster Deployments, and are also linked
to a group of users with designated roles.

## Advanced Features

### Policies

Bundles of permissions that are assigned to roles - for example `Manage self`, `Create teams`,
`Manage team deployments`.

### Permissions

The lowest level of our model is the permissions center around objects and
actions, for example: `user.delete`, `team.create`, `deployment.list`.

[Full list](https://github.com/astronomerio/houston-api/src/database/migrations/20180619163410_rbac_seed.js)
