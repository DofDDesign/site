---
layout: blog-post
author: Joptimist
authorURL: https://github.com/JoshMcGiff
title: Pawns, Characters Not Moving
excerpt: DefaultSceneRoot override issue - Unreal Engine 5 - After many painstaking hours of debugging, we discovered that DefaultSceneRoot can be the ROOT of all evil… **badum tss**
date: 2024-05-14 22:55:07.301013 Etc/UTC
pinned: false
keywords: Unreal Engine, UE5, Unreal Engine 5, Bug, Bug Fix, Default Scene Root
category: Unreal Engine 5
---
I am currently working on a turn-based RPG gamemode for my own game development project.
This gamemode involves an exploration section that encourages the player to explore an
expansive environment. Along the way, they can encounter free-roaming enemies that, upon
colliding with them, initiate a battle level. This logic for triggering a battle with an enemy is
relatively straightforward. By implementing the OnOverlapBegin function on the player, the
collisions are handled.
This was all going swimmingly, until I wanted to experiment with the “AI” & BehaviourTree
mechanics within Unreal Engine 5. I wanted to add the free-roam nature to the enemies.
Therefore, I followed the existing UE documentation to create a simple “MoveTo” behaviour that
enabled the enemies to move around the navigable area within the level. I added to this to
enable the enemy to move towards the player, if they were within vision of the enemy itself.
Upon testing my newly created near-sentient “AI”-power<img src='{{ site.baseurl }}/3499608151781539851715744961475638-0.gif'/><br><img src='{{ site.baseurl }}/3499608151781539851715744961475638-2.gif'/><br><img src='{{ site.baseurl }}/3499608151781539851715744961475638-1.png'/><br><img src='{{ site.baseurl }}/3499608151781539851715744961475638-3.png'/>
