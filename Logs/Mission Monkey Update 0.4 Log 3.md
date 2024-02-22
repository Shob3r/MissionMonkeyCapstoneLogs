
It's been quite a bit since I wrote log 2. one of the most important features of the entire game is nearing completion day by day, and that feature is the brand new AI system. I wrote most of my ideas of the AI system in [The notes I wrote]([[How The Enemy AI System Will Be Designed]]) before I started work on the new AI system, but it has slightly changed since I wrote that plan. So, in this log, I will be covering in-depth how my AI system works, and also talk about a few other things that I have updated since log 2.


## Enemy Sight

Enemy sight a crucial step to get right in the new AI system. There have been two previous AI systems before this one and neither of them could get it right. So, I decided to try using a feature of the Unity Game Engine I have never used before now, known as a SphereCast. 

A SphereCast is an invisible sphere that reports what objects are within the sphere to a script using it. I prefer this over a Raycast (Same concept but instead of a sphere, it's a one-dimensional line being created instead) for base player detection. 

However, halfway through writing the code for Enemy sight, I noticed that the player could still be detected through other objects, so I decided to also create a secondary check for the player using a Raycast. Every instance of the Enemy Sight script contains the precise location on where the player is at any given time. if the SphereCast detects that the player is within its confines, It will then fire a Raycast straight to the player and check if the Raycast actually hit the player (The Raycast cannot "see" past anything it hit)

This works perfectly, but I also noticed after completing the script that the detection points sometimes can have "Dead-zones", where the player should be detected, but isn't because it's in a strange position for the script. So I also decided to make it possible for an AI to have multiple Detection points on it. This finally makes AI sight detection work perfectly

Below are visualisations of my explanation:
![[Pasted image 20240218110719.png]]
![[2024-02-18 10-38-04.mp4]]

Needless to say, I am very pleased with the outcome of the detection system
## Enemy Navigation


## Enemy Attack

## Enemy State Manager

The Enemy State Manager Script Imports all of the other scripts required for an enemy, and manages 
## Enemy Animation Manager


## The other thing I did in my project: The brand new save/load system

Dear lord the old one SUCKED. but the new one is incredible. it works exactly the same as my old system, but the code is much more clean and accessible to the rest of the project. absolutely worth the two days I spent on it-


# What Am I Working On Next?

With the AI system, the base code for the game is now complete. I will now start work on the actual gameplay of chapter 1. I have been working on other features for far, far too long and I am running out of time for the meat of the project, where I can showcase my 3d modelling and animation skills as well as my ShaderGraph skills that i'll learn when creating surfaces


