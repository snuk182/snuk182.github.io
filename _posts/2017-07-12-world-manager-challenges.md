---
layout: post
title: World Manager challenges
description: What needs to be done.
github_comments_issueid: "2"
excerpt_separator: <!--cut-->
---
Given:
 1. A set of universes, each has own chunks and entities.
 2. Each of the entities has its own view distance. The range of the universe (chunks) visible to the entity is called World.
 3. Entities move unpredictably (no way!) -> their worlds should be updated **as fast as possible**
 
<!--cut--> 
What failed:
 1. Loading all the entity world's chunks, moving its bounding box with calculation of difference of old and new world -> **too many chunks to check and update = too inefficient**
 
What to try 
 1. Loading only the accessible chunks -> a sophisticated mechanism of chunk management is required, per-entity per-universe, and taking all the entities into account at the same time
 
#wnd #rust #gamedev 
