---
layout: project
date: 2019-02-02
title: NYCIML Scores
---

## NYCIML Scoring

### Links

* <a href="https://scores.nyciml.org" target="_blank">Website</a>
* <a href="https://github.com/alexlu876/iml-scoring" target="_blank">Source</a>
* <a href="https://pypi.org/project/graphene-cerberus" target="_blank">Graphene-Cerberus</a>

### Technologies Used

Python, Typescript (+ JSX), Flask (+ flask-session, Flask-JWT-Extended, Graphene and SQLAlchemy extensions) GraphQL (Graphene for server, Apollo Client for client), MySQL (SQLAlchemy for ORM, relational database with ~19 tables), React (+ MobX for stores, Material UI for front-end components, Apollo for GQL queries/caching).

### Description

A scoring website for IML/ARML-style individual-round mathematics competitions, employing Flask, SQLAlchemy, and Graphene for providing a GraphQL API for our front-end. Made along with a custom validation system to elegantly combine the Cerberus validation library with
Graphene. Developing a React front-end to replace an older Jinja prototype, with Apollo Client and MobX for fetching, caching, and state management. The website is used by coaches to manage teams and students, and upload contest scores to be viewed by the public.

<!--more-->
![NYCIML Scoring](/assets/img/nyciml-1.png)

![NYCIML Score Viewing](/assets/img/nyciml-2.png)
