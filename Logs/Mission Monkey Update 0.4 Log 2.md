

In the past few weeks, I have worked on the all-new UI for the game. While it will change a little more over the course of the development cycle of this update, it's mostly at the point where I want it to be for the foreseeable future. 

# Save data information get script

A much smaller thing that I have worked on in the last few weeks, but it plays an extremely important role for the UI, and for other parts of the game in the future. This script will attempt to return relevant information from the script and then converting the returned information to either a string (a set of characters) or an int (a whole number)

It took me a few hours to make, but this is really the thing I really liked working on for this section of the development cycle. Click [here](obsidian://open?vault=Mission%20Monkey%20Notes%20and%20Logs&file=Screenshots%2FSaveInfoGetterCodeSnippet.png) to view a complete snippet of the file
# Player UI
![[PlayerUI.png]]
Pretty simple, but it works for my needs!
## Health Bar
![[HealthBar.gif]]
Pretty simple to explain, the bar changes it's fill percentage and colour depending on the total amount of health the player has. (The transition is also really smooth thanks to the Mathf.Lerp() function Unity Provides)

## Ammo Count Bar
(picture of it can be seen in above GIF)

Currently non-functional, as I am yet to program in the ammo system for each weapon. Once that has been implemented though, the bar will behave similarly to the health bar, except instead of showing how much health the player has left, it's how much ammo the currently held gun has left
## Objective UI
![[ObjectiveUI.png]]
It will show the current task the player has to complete to progress through the story. I have written scripts to change the current objective on the UI. Unlike other games, which also have an icon for the objective location on screen (with distance), this game will not have it ~~because I'm lazy~~ because I want the player to visually navigate around the level to find the objective. This will of course mean that when the time comes to start building Chapter 1 (after all the code gets written), I will have to pay a lot of attention to the scenery in the level to point to the right place  

# Main Menu/Pause Menu

![[MainMenuScreenshot.png]]

I don't know what this style should be called, it kind of just popped into my mind one day, so I kept the idea in mind when designing the UI. I think it looks really good and is one to one with my idea.

the sub-menus are listed below, but the main menu has a few functions too. First off, clicking the Discord and GitHub icons will actually open a link in your web browser to the respective pages. Secondly, clicking on the little version text below the title will open up the new version sub-menu (which will be talked about later)

In the future, I will create a 3d model for the location of the first chapter. I also intend to make the scenery in the main menu change on each chapter change (what is loaded is decided by the save data info get script)


## New Game Menu

This menu shows whenever the player wants to start a new game. A menu containing all the playable chapters will show and the player can select one of them as the starting point. Once I get to developing more chapters of this game (after capstone), I will make sure that the player can only select later chapters in the game if they have already played through the game once.

This UI is waiting on a slight overhaul after some basic level works have been completed on Chapter 1, so it's mostly the exact same thing all the way down

## Save/Load Game Menus

![[LoadSaveMenu.png]]

These menus will show the player information about the saved data and ask the player weather they want to overwrite the save with current data, or weather they would like to load the save data. These menus both use the save data information get script mentioned above

## Options Menu

![[OptionsMenu.png]]
Pretty simple compared to the options menus of other games, but I do not expect this game to really need more for the time being. In this menu, you can change the following:
- The quality asset
- The anti-aliasing mode/quality
- The subtitle settings (WIP, coming after i finish subtitle system & dialogue)
- The volume
- The camera's field of view
- The mouse sensitivity of the camera

All of these options are stored in the registry of the computer and are loaded back up whenever the game launches

## New Version Update UI

![[UpdateMenu.png]]

This is done by comparing last played version on the save data of the player (which now has a field to indicate the last played-on version) to the current application version (which is set in Unity). if they are not the same, then this UI will show. It can also be manually toggled by clicking the version text under the title.

# Death Screen

![[DeathUI.png]]

As you may see, the UI is pretty simple, and I like it that way. Once all the big systems are coded in, I will make a transition to this UI in the form of the "VHS static turn off effect" once the player dies. 

# Did the Trello page help?

In log 1.5, I mentioned the use of Trello to keep my tasks organised. So did it help? The answer is **YES**. I am so happy I decided to organise my tasks this way. Feels good to move a task to the "Completed" tab on the page. I would 100% recommend using Trello for any large project the reader may have, it really helps me stay on top of things


# What's next?

Since I have essentially completed the UI for the time being, I think I should move on to more important systems for the game and actually start seriously programming. Therefore, I have decided to begin working on the **Enemy AI System** next. 

In previous versions of this project, we had AI, but it was very stupid. It didn't really have any decision making, and defeating them was as easy as running around them in circles. The "Mission: Monkey AI system 3.0" (a name I just came up with) will have more realistic AI, as well as possibly a difficulty modifier (If it doesn't take 3 months to implement!)

Secondly, in the near future, I will find a way to redesign the current logo and "promotional material" of the game, as the current one was supposed to be temporary anyways and looks kinda bad. It will probably be introduced in log 3

Finally, I'm still 100% confident in being able to finish this on time. It will happen.
