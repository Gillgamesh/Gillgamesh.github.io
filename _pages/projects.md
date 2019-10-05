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
    - [FTC Relic Recovery Robot](#ftc-relic-recovery-robot)
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

The map editor allows you to assign custom travel weights to each grid block/pixel,in addition to walls and the start/end point. After choosing your algorithm from one of the default two, the simulation opens up where you can pause, slow down, fast forward etc. A full list of features and tech specs can be found in the [SRS](https://gitlab.com/Gillgamesh/cse-160-final/blob/master/Pathfinder-SRS.pdf).

For example, heres a visualization of the pathfinding without a distance heuristic--more expansion is performed on the top left corner:

![Pathfinder Dijkstra](/assets/img/pathfinder-dijkstra.gif)

Compared to a weak distance heuristic that is still admissable, which does a slightly better job of not exploring corners that increase your heuristic cost. Keep in mind, that although these examples are using A\*, in reality any shortest-path or path-finding algorithm can be implemented and visualized (and I'm planning on implementing this as a library that can be used on any WeightedGraph<> interface as defined in the source).
Although there are slight differences in the final path, both had the same total cost.

![A\* Distance](/assets/img/pathfinder-astar.gif)

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

A Go-based 3D graphics/animation renderer with primitive concurrent CPU-based matrix library (it'll max out all your cores, but its still pretty bad compared to using a GPU for 4xN matrix multiplication), support for lighting and shading, and rendering basic Wavefront files through a custom rendering language. Written primarily for a class on Computer Graphics at Stuyvesant. 

Here's some examples of some images that were rendered using this project, they're pretty cool. The first one was inspired by the rings from Halo, which orbit a larger gas giant. The third is just your typical Utah teapot wavefront file and a random pear we found on the Internet. The second is literally just a ball rolling. By editing the `gourd.mdl` file you can make much more amazing demos with multiple light sources, more objects, etc. 

![Halo2](/assets/img/halo2.gif){: .center}

![Rolling](/assets/img/rolling.gif){: .center}

![lightshow](/assets/img/lightshow.gif){: .center}


## Boneless Relativity

### Links

* [Source](https://gitlab.com/Gillgamesh/boneless_relativity)

### Description

A basic 3d particle physics simulator that does electromagnetic and gravitational forces. The simulation is done in Planck units (G=Ke=Kb=c=1) with each pixel equivalent to a planck length. Still demonstrates inverse square law. For sake of demonstration, editable modifiers have been added to magnetic, electric, and gravitational forces, with the default values being the ones found to be most interesting.
ie without the modifiers, with m=v=q=1 for both particles, gravitational and electric force are equal in magnitude, and assuming the particles to be parellel as is the magnetic force (this will likely not be the case after a while though) (you could specify a modifier for the strengths of each field, or set the charge to 0 to get a gravity simulator). Uses Processing's 3D rendering service and ControlP5 to save setup time. Really useful demonstration for classroom environments; made for my AP Physics C class senior year.

As an example, here's two charges with equal charge and mass, but one has a velocity slightly less than the other:while we initially have an oscillation due to gravitational/magnetic attraction vs electric repulsion, as their slightly different velocities and resultant difference in x position build up, we see that the oscillation along the y axis disapears. Here, the green gives you the gravitational force, blue the magnetic field direction, and the red the electric
force:

![Boneless Relativity](/assets/img/boneless-relativity1.gif)


## FTC Relic Recovery Robot

### Links

* Some of the code [source](https://github.com/gillgamesh/relicrecovery).

### Description

Although we didn't do too great in competitions with this bot due to some poor timing, Stuy Fusion's 2018 robot for the FTC Relic Recovery competition was really fun to work on and had a really cool mechanism that I really loved designing and building: the mecanum wheel glyph lift. By using mecanum wheels with 45 degree rollers, we were able to intake blocks with the same system we lifted them up, saving space and surprising parents and kids at demo
events with a mechanism they hadn't seen before. Here's a demo of our intake from the 2018 FRC NYC Championship, where we worked directly with [NYC FIRST](https://www.nycfirst.org/) to demo our robots and let kids drive them around:

![FTC Bot Glyph Pickup](/assets/img/ftc2018-1.gif)

In addition to programming the robot for competitions (including some cool tech like a phone-camera based CV system for detecting the color of one of the scoring elements in the game; and some work with hall effect encoders and gyros put together with a PID loop giving our mecanum drivetrain really smooth turning) and wiring up the electronics I did most of the design work and building on the intake and drivetrain. I created a (much prettier) CAD of the intake that used CNC'd parts, bought the
necessary bearings, belt pulleys, and motors for the intake (in addition to the rest of the robot), and worked with a teammate to cut and drill some janky parts that we couldn't get CNC'd due to to logistic issues. After we put it all together and perfectly adjusted the tension on the arms (the distance between each side of the intake expands when force is applied due to surgical tubing that acts like a spring), we got this impressive result.

---

# 2017

## EmenbeeAntiCheat

(Source Unavailable)

### Description

Based off an idea and previous attempt by [Emenbee Realms](https://www.emenbee.net/) owner and late friend Bryan, EmenbeeAntiCheat helped tackle a big problem with running Minecraft servers with PvP features/gamemodes. 

Because it is incredibly easy to install custom minecraft clients/mods and because the vanilla minecraft server/client configuration has no built-in client validation system/client-side cheat detection like you might find in League of Legends or some other game, cheating is incredibly prevelant. Some of the more obvious cheats--flight, speed, etc. are easy to check and covered by publically available plugins for Bukkit, the de-facto standard API for custom Minecraft servers.
Others, usually involved with hitting other players in melee combat, are incredibly difficult to catch with traditional methods because of the complexities and variation in playstyle making false positives on anti-cheat systems incredibly high. By using Encog for Java, along with the Bukkit API's hit event/player position features, we came up with a strategy for using CNNs to deal with this detection.

To provide some context, combat in Minecraft was an incredibly important aspect of Minecraft server communities from 2013-2018, and was surprisingly competive. Servers would go as far as adding ranking systems for combat (I wrote a plugin that added an Elo system to one of our servers that were specifically meant for PvP), and even very lowkey cheating would be enough to make people quit servers for making the PvP aspect frustrating. 
Minecraft PvP (before the controversial 1.9 Combat Update) is effectively cookie clicking (where how fast you click is incredibly important compared to, say timing in an FPS with recoil or bloom), paired with no-lag aiming (your hits register almost exactly where you look, almost instantly/ hitscan except for melee), and some weird movement tricks (sprinting and hitting people might help you get critical strikes, for example). It's surprisingly addicting and competitive, and there is a lot of room for skill to make a difference in the result between fights given two people with identical items.

There's several types of clients that help players cheat in terms of PvP. The simplest is auto-clicking, where the client essentially clicks incredibly quickly but sometimes with some randomness for the player, so they can focus on aiming (this has traditionally been the hardest to catch, and even with our AI anti-cheat wasn't fully dealt with). 
The more complicated system is kill-aura, where either clients try to register hits on players despite not even looking at the opposing player. Variations of this incldue systems that auto-aim instead of trying to regsiter invalid hits, for example quickly jerking the cursor to some location in the hitbox of the player, rather than instead of just pretending to do so.

By having our neural network examine how people play with cheats (i.e. by getting a bunch of people on a test server to come on and use popular modded clients to give a supervised learning training set), with inputs measuring a batch of 10 hits for differences in player orientation, velocity, time passed, distance between player and opponent (Minecraft allows hits to register from anywhere from 3m to 4.5m away in a vanilla context with some randomness, and these clients will try to get further hits more often), 
and hitbox inaccuracy (how far the player's orientation is from the center of their opponent's hitbox), we were able to classify with 90% accuracy what type of combat-cheats people were using (and higher accuracy for vanilla players, i.e. we were unlikely to misclassify whether someone or cheated or not, but somewhat likely to confuse obvious autoclicking or two types of kill aura). 

After making a very primative version with Bryan, my future innovations on this system were to classify batches of hits rather than a single hit
(letting us see change over time and possibly detect patterns for random autoclickers), and
look at more properties than just hitbox inaccuracy. Unfortunately, Bryan passed earlier in 2019, and because of his initial contributions to the codebase and ownership of Emenbee Intellectual Property, and out of respect for his initial desire to keep the code private, I'm unable to provide the source code. However, if anyone would be interested in more details of how we went around implementing this and how successful our process was, feel free to hit up my Email!

## Cuties CV

### Links

* [Github](https://github.com/dariashifrina/cuties)


### Description

Cuties Computer Vision (CCV) is a basic implementation of Computer Vision. Developed by James Smith, Dasha Shifrina, and myself, this program allows you to track an object or run a sobel edge detection filter on a pre-recorded video or a live camera feed. This program relies on keeping track of a single object via it's color using its hue, saturation, and brightness components(HSB).

In order to run it, you will need Processing, its corresponding Video library, and GStreamer. Generally, you can load either a video or webcam footage, click on an object to track, and optimize the settings using the keyboard shortcuts listed in the Github repository. 

Our strategies for Sobel filtering and HSB filtering are incredibly rudimentary, using erosion and dilation helps deal with some of the noise. That being said, the performance still suffers, partially because the amount of filtering we are doing but also because processing is done in a single loop with no concurrency. This was also made in our junior years of high school, so our programming intuitions and thought process weren't exactly the best, but overall it was
still a really cool project!

Here's a small demo of object tracking, and you can find more examples of our HSB and Sobel filters inside the repository:

![Cuties CV](/assets/img/cuties-cv-1.gif)

---

# 2015/2016

## MaGiC

### Links:

* [Source](https://github.com/matteowong/MaGiC)

### Description:

A remake of "Mastermind," made with Matteo Wong and Caleb Smith Salzberg for AP Computer Science. My main contributions were the incredibly jank code-masking system and contributions to the thought process writing an "algorithm" for our rudimentary brute-force solver.


## Handy Hotspot NYC 


---
