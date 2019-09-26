---
layout: content
title: Projects
permalink: /projects/
---

I've decided to include all of my major projects that are at least what I'd consider a minimal viable product, going all the way back to my Sophomore year of high school in 2015 to today, instead of just the projects I would show off to recruiters or friends (labeled \*). It's awesome to see how much better I've gotten with structuring code in readable ways, and being able to work on larger scale projects, but of course I've still got a lot to learn. 

Many of these projects were originally for school and have only been slightly modified from that state, but they're still a decent showing of what I'm about. That being said, I'm especially proud of the projects that were done on their own voalition (labeled \*\*), because they were most true to how I see software--finding a problem, and learning how to use and create the tools best fit to solve them. 

- [2019](#2019)
    - [NYCIML Scoring](#nyciml-scoring)\*\*
    - [Pathfinder](#pathfinder)
- [2018](#2018)
    - [StuyActivities.org](#stuyactivitiesorg)\*\*
    - [Go Graphics Engine](#go-graphics-engine)\*
    - [Boneless Relativity](#boneless-relativity)
- [2017](#2017)
    - [EmenbeeAntiCheat](#emenbeeanticheat)\*\*
    - [Cuties CV](#cuties-cv)\*
- [2016](#2016)
- [2015](#2015)

---

# 2019

## NYCIML Scoring

### Links

* <a href="https://github.com/alexlu876/iml-scoring" target="_blank">Source</a>
* <a href="https://pypi.org/project/graphene-cerberus" target="_blank">Graphene-Cerberus</a>

### Technology Used

Python, Typescript (+ JSX), Flask (+ flask-session, Flask-JWT-Extended, Graphene and SQLAlchemy extensions) GraphQL (Graphene for server, Apollo Client for client), MySQL (SQLAlchemy for ORM, relational database with ~10-15 tables), React (+ MobX for stores, Material UI for front-end components, Apollo for GQL queries/caching).

### Description

Creating a scoring website for IML/ARML-style individual-round mathematics competitions, employing Flask, SQLAlchemy, and Graphene for providing a GraphQL API for our front-end. Created a custom validation system to elegantly combine the Cerberus validation library with
Graphene. Developing a React front-end to replace an older Jinja prototype, with Apollo Client and MobX for fetching, caching, and state management. The website will be used by coaches to manage teams and students, and upload contest scores to be viewed by the public.

Here's some photos from the working front-end prototype, which was made using Jinja, some really janky JS and jQuery, and MDC. The final website will look similar (and include the watermelon coloring!), but will be easier to expand and will feature a much richer and cleaner set of tables and tabs for adding, editing, and removing (something that was a problem last time I used a similar stack for [StuyActivities.org](#stuyactivitiesorg)).

![NYCIML Scoring](/assets/img/nyciml-1.png)

The scoring table is seperated per team-contest pair, and has a limit on how many students can have scores entered determined by NYCIML admins. Afterwards, all the scores are uploaded to our database, and can be viewed or downloaded from a contest-specific page. The backend theoretically supports doing non-ARML formatted contests (for example, having multiple points per question or doing team score only contests). 

![NYCIML Score Viewing](/assets/img/nyciml-2.png)

## Pathfinder 

### Links
* [Source](https://gitlab.com/Gillgamesh/cse-160-final)

### Description

A JavaFX-based visualizer for pathfinding algorithms on a 2D grid. Weights can be specified per grid square, and the cost to travel between 2 adjacent grids is the average of their weights. Includes a map editor, allows for map files to be saved for later use, and includes a simple-to-use interface for including your own path-finding algorithms (still working on being able to import it into projects easily). Great for visualizing how specific pathfinding algorithms might be
more efficient than others (for example, A\* with a distance heuristic will open the opposite direction less frequently than without a distance heuristic).

---

# 2018

## StuyActivities.org

### Links

* [Website](https://stuyactivities.org)

### Description

StuyActivities.com, a fully fledged after-school activity manager for high schools. Built in Python 3 using Flask, Amazon S3, PIL, and SQLAlchemy. Robust front-end that uses WTForms, Jinja, jQuery, and various JS libraries. Easily expandable and maintainable, and is actively used by over 3500 students and faculty members. Features a club chartering and approval system, meeting and attendance management with personalized and global calendars for students, and a built-in room reservation system. Students can join and create clubs online, can request funding from the Student Union or Parent's Association for their organizations, and can get information out to their members all from one convenient site.

Although my active development on the website has ceased as of November, I continue to serve in advising role for big technical decisions such as making significant changes to one of the dozens of essential tables or adding new features such as an OAuth 2.0 server.


## Go Graphics Engine

### Links

* [Source](https://gitlab.com/Gillgamesh/finalgraphics/)

### Description

A Go-based 3D graphics/animation renderer with primitive multithreaded matrix library, support for lighting and shading, and rendering basic Wavefront files through a custom rendering language. Written primarily for a class on Computer Graphics at Stuyvesant.

## Boneless Relativity

### Links

* [Source](https://gitlab.com/Gillgamesh/boneless_relativity)

### Description

A basic particle physics simulator that does electromagnetic and gravitational forces. The simulation is done in Planck units (G=Ke=Kb=c=1) with each pixel equivalent to a planck length. Still demonstrates inverse square law. For sake of demonstration, editable modifiers have been added to magnetic, electric, and gravitational forces, with the default values being the ones found to be most interesting.
ie without the modifiers, with m=v=q=1 for both particles, gravitational and electric force are equal in magnitude, and assuming the particles to be parellel as is the magnetic force (this will likely not be the case after a while though). Uses Processing's 3D rendering service and ControlP5 to save setup time. Really useful demonstration for classroom environments; made for my AP Physics C class senior year.

---

# 2017

## EmenbeeAntiCheat


## Cuties CV

---

# 2015/2016

## Magick (the Game)

## Handy Hotspot NYC 


---
