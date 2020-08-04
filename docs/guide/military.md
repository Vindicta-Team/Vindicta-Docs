---
layout: default
title: Military
parent: Guide
nav_order: 9
---

# Military
{: .no_toc }

In Vindicta you are fighting against the forces of your own government.  
These forces are divided between the [police](police), and the military.  
While the police are very limited in their reactions to you, the military are not.  

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Disposition

At the start of the game the military will occupy all airfields and bases, and some randomly selected outposts.  
Airfields will have 3 officers present, and bases will have 1.  

## Aggression

Aggression level varies between 0 and 100% and can be seen at the top of the map UI.
Aggression influences following aspects:
- Willingness of commander to occupy cities and capture other locations.
- Willingness of commander to deploy roadblocks.
- Willingness of commander to bring more heavy vehicles (MRAPs, APCs, tanks, helicopters).
- Willingness of commander to fight for territory.
- 'Propaganda' rate - the higher the aggression, the faster you start losing influence on cities which are not occupied by your side. This is done to simulate various propaganda methods the enemy can imploy to mobilize civilians.

## Regeneration of units

Military forces of the enemy are regenerated in the following way:

- Soldiers are aquired by same recruitment mechanism as for player side. So, it is **crucial** to destabilize and capture cities to prevent enemy army from reinforcing itself.
If you own some portion of the map, don't overestimate the amount of people which can be mobilized over time by the remaining large amount of enemy territory.
- Vehicles are brought in only through airfields, and are later redistributed elsewhere.

## Officers 

Officers are the sub-commanders of the enemy military.  
The enemy cannot launch an offensive action from a location unless an officer is present there.  
The enemy will attempt to ensure all garrisoned locations have an officer assigned, prioritizing based on size.  

## Intel

The commander is subject to the same rules on intelligence as the player.  
They can only know about a location if they have discovered it by some mechanism, direct observation usually.  
Knowledge of your movements and location is determined by oberservations made by the commanders units, 
and only as accurate as the last obervation that was made.  
If you have a group of four units, and the enemy only sees one, they will only know about that one 
(although they may guess that there are more).

## Actions

The commander has many actions at their disposal, and will decide between them based on an analysis of the intel 
the commander has available, and the currently commander strategy.  

### Quick Reaction Force (QRF) 

This is the basic response to the enemy spotting you. The commander will send a force of appropriate size to investigate 
and engage you. The source garrison for the QRF is determined by a combination of the distance and forces available.  
These actions are deployed rapidly, you can expect them to arrive within minutes of your discovery if an enemy location is close.  

### Reinforcement

The commander determines the force level required for a location by a combination of the threat you pose in that area, and 
the location type itself. If a garrison falls below the force level required (or the force level required rises due to your 
activity), the commander will consider sending reinforcements from another garrison.  

### Take

Depending on strategy the commander may decide to take certain locations. They will send an exploratory force to capture and
occupy the location, followed later by further actions to supply the location, and assign it an officer.  
These actions take some planning, and as such the delay before they begin tends to scale with the size of the force, and 
the distance to the target location.  

### Build Roadblock

In areas of high activity the commander will deploy roadblocks from local outposts.  

### Assign Officer

Officers will be assigned to bases and outposts from airports, prioritized by the size of the garrison.  
It will take a while for the officers to put their affairs in order before moving to another assignment, thus these actions can be delayed by a few hours.  

### Patrol

Enemy outposts and bases will deploy routine patrols to the surrounding towns. These can deplete the forces at the location they
are dispatched from significantly.  

### Supply Convoy

Convoys of various kinds will be sent out regularly from airfields to bases and outposts held by the enemy (if they have an officer there to request them).  
These will contain bulk amounts of various items, including:
- Building supplies
- Primary weapons
- Secondary weapons
- Medical supplies
- Explosives
