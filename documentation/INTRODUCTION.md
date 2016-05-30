![WorldEdit](img/logo2.png)
=========

# Introduction

This project is for a college subject (Software Arquitecture), and we want achieve
some goals like:

* [4+1 Architectural view model](https://en.wikipedia.org/wiki/4%2B1_architectural_view_model)
  * [Logical view]()
  * [Development view]()
  * [Process view]()
  * [Physical view]()
  * [Scenarios]()
 
Our introduction chapter, will be divided under two sub-sections, an user and developer introductory view:

##User View

###[WorldEdit? What it is?](http://wiki.sk89q.com/wiki/WorldEdit)

WorldEdit is a world editor for Minecraft which makes users life way more easy by helping on some essentials things in
game, like building structures, spawning objects, and manipulate them, among others. In this analysis we will talk about about how this in-game framework works, and how it is implemented "behind the hood". It holds some interesting features:

* Select a region of a map (like pinpoint two positions in map)
* Fix map problems, such as broken water, missing snow, broken walls and much more!
* Make big constructions with two clicks
* Change blocks from one type to another, like from grass to diamond
* Create objects with one click, e.g, trees, spheres, animals

We aim to include different architectural views (more exactly, 4+1 Architecture view),and his stakeholders. During this analysis, we pretend to discuss about how we could improved this framework, contributing to the software and future developers.

##Developer View

In terms of developer view, and avoiding to spoil any conclusions, we want to get into some aspects of Minecraft itself.

Minecraft was made in Java, and it's world is composed by chunks. Chunks are 16x16x256 segments, and they are generated around players when they first enter the world. As they walk around, chunks are generated as needed. They can also be forced to load into memory by world management tools, such as World Edit.

Our architecture views along this documentation, will describe how the main components communicate with each other. Starting on the logical view up until the physical view, we can get really deeper into the structure of the project.

* In the logical view, we will feature a class diagram with a description of some of the main classes or packages.
* By the development view, a full described package diagram with the programmers prespective.
* The process view will walk us by the activity diagram and behaviour.
* In the physical view, the system from a system engineer's point of view. Deployment diagram will feature the topology of software components different from the last views.
* The last view, show us some use-cases of WorldEdit.
