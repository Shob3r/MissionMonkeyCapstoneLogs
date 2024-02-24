
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

Enemy Navigation is a pretty simple script. While the player has not been noticed, it will navigate around a set of "Patrol points". Once the player is seen however, it will follow the player until it is destroyed. I was going to make it slightly more complicated like how i explained in my plans for the system, but it would take way too much time than what i currently have available to me (90 days), so the way it navigates right now is fine

## Enemy Attack

Once again, this script is much more simple than the enemy sight script. this script fires a Raycast towards the player once every x seconds (x being a value that I can set for each AI in the game. currently the default is 0.25 seconds) if the player is in the AI's attack range. Each time the ray is fired, also play the sound effect attached to the script. 

If the Raycast hits the player, deal a predefined amount of damage (Working on random damage too). If not, wait until the script runs again


## Enemy AI stuff I will need to do later or after the capstone is over:

The current state of the AI system is very, very good, but it is still missing a few things. I would love to finish these but I fear I may not have time for the meat of my project, which would be a total remake of chapter 1. So these features will be worked on alongside the new chapter 1 or will be done after capstone is over when there is no more time crunch on my back

- AI Animations (This will happen before capstone is over)
- AoE (Area of Effect) attacks (most likely after capstone)
- Ambient sound effects of the AI (Will happen before capstone is over)
## The other thing I did in my project: The brand new save/load system

Dear lord the old one SUCKED. but the new one is incredible. it works exactly the same as my old system, but the code is much more clean and accessible to the rest of the project. absolutely worth the two days I spent on it-


# What Am I Working On Next?

With the AI system, the base code for the game is now complete. I will now start work on the actual gameplay of chapter 1. I have been working on other features for far, far too long and I am running out of time for the meat of the project, where I can showcase my 3d modelling and animation skills as well as my ShaderGraph skills that i'll learn when creating surfaces


# Other things


## New Lemon Studios Logo

I am currently in the process of redesigning the logo of the organisation which Mission: Monkey is a part of (don't know how to phrase that one). The old one was good and all, but I made it all the way back in grade 9 and it just looks quite bad compared to what i'm working on right now

I created the new logo using skills I learned in Content Creation and Digital Marketing 


Current Logo (The Old one):
![[Pasted image 20240224011528.png]]
New Work-In-Progress Logo (Not Final)
![[Pasted image 20240224011543.png]]
## Lemon Studios Launcher

This isn't related much to my capstone project, but a friend of mine has decided to create an application that allows users to download projects created by lemon studios (currently, the only project that can be downloaded is Mission: Monkey, so that is the only game tab). I am not working on it currently, but after capstone is over, I will almost certainly be creating back-end infrastructure that will be used with this launcher. 

Here is a screenshot of what it currently looks like: 
![[Pasted image 20240224011956.png]]