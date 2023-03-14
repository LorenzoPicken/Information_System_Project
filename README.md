# Information_System_Project

## Project Proposal

> What Game Have I Chosen?

	The game I’ve decided to go with for this project is “Friday Night Funkin’: Hypnos’s Lullaby”, a 2D, cartoon style rhythm game made by members of the community as a mod to the original game simply known as “Friday Night Funkin”. This mod is based around the theme of Pokémon, but doesn’t follow its light-hearted and kid friendly nature. It instead uses disturbing imagery and sound design, warping many familiar faces from the Pokémon franchise into creepy, demonic looking beings who harbour ill intent towards the player. As is the original game, this mod is also a rhythm game that shares many similarities to other video games in this category, namely the Dance Dance Revolution series. In time with the music, the player will need to match the arrows on screen with the correct arrow keys on their keyboard as they try and complete the song without their health dropping to zero.

Why Did I Choose This Game?

	Aside from the very pleasing artwork and catchy musical scores found within the game, “Hypnos’s Lullaby” holds a very special place in my heart as it introduced many new and refreshing gameplay elements to the series, making it one of the hardest mods to master. The tone is also a lot more sinister and intriguing than that of the original “Friday Night Funkin”, which caught my attention. Finally, as a musician myself, music is always something that I love in games and in real life. I am currently working on my very own project which involves the creation of a rhythm game, very heavily based on this series, as well as composing my own scores in a similar style to the music found in this game. As such, I thought it would be only fitting to do this project on “Hypnos’s Lullaby” as it may help me in the future when I start coding my game.

Game Scenario

		For this project, I will be focussing on the gameplay of a specific song. “Monochrome”, composed by Adam McHummus, it is the third and final song in the second level of the mod where the player faces Gold. Gold is the user’s character in the first section of Silver, the game's second level. After dying at the end of the song “Frostbite”, he comes back as a corpse, possessed by an unknown force, having lost all his limbs, his eyes and covered in his own blood, now turned black from decay. I’ve chosen this score as it has one of the most challenging mechanics in the mod and is widely considered by many to be the hardest section of the entire game. “Monochrome” stands to be, to this day, the only song I personally have not completed in Hypnos’s Lullaby even after over 100 separate tries. This is because of the song's main mechanic. During many of Gold’s sections, text will appear on the screen, written in a very cryptic and hard to read font. The player must be able to decode the message and type it into the game before Gold finishes singing. If the user fails to do so, gold disappears into the darkness and the player is forced to start the song all over again. What makes this especially hard is the fact that there are over 50 different random message combinations and, since the mod was cancelled right before release, special characters such as exclamation points and interrogation points are simply impossible to input as this feature was never coded into the game. With this monstrous gameplay mechanics, the creators also implemented jump scares which will queue at set times during the score, obscuring the screen for a moment. Finally, a dead Pokémon appears three times throughout the song, each time, reducing the player’s max HP by 20%. “Monochrome” is one of the few two-phase songs in this mod, where, in the middle of the song, Gold says “No More”, two small red eyes then appear from inside his skull, visible through his empty eye sockets, followed by the unknown force taking possession of his head and tearing it off his torso, his spine going with it. From this point one, the chart becomes significantly more difficult and jump scares happen much more frequently.




## User Story

> ●	As a user, I can use the arrow keys/ WASD to activate notes
●	As a user, when I activate notes on time, I can get points
●	As a user, when I miss a note, I lose health and get a miss on my miss counter
●	As a user, when I hit a note, I can gain HP
●	As a user, I can see my health, score and misses
●	As a user, I can type during the typing sections using my keyboard
●	As a user, I can pause the game at anytime, aside from during typing sections (avoid cheating the mechanics)
●	As a user, from the pause menu, I can resume, restart or quit to the main menu
●	As a user, when I lose, I can return to the menu or retry the level


## Flowchart Diagram

>The game will first Load in the level and then will next play an audio que paired with subtitles followed by an animation of the enemy appearing into frame. Now in the play area of the game, the user will be given their controls to activate their arrow hitboxes and the music will start. A timer will start, invisible to the player, which will trigger specific scripted instances when time thresh holds are met and will determine the player’s victory if the user is still alive when the time expires. These scripted instances include Jumpscare Event, Celebi Event, Typing Event, Phase2 Event and note spawning. 

### NOTE SPAWNING 
	Note spawning is a reoccurring event which will spawn the chart that the player must complete. During this time, the enemy character will constantly loop through an idle animation while they aren’t in motion. As the notes pass by, the player will be expected to activate them before they arrive at another hitbox which automatically destroys them. Depending on if the note is destroyed by the player or by the automatic hitbox, the game will determine if it is a miss or not. If it is a successful activation, the game will play a success animation using the player’s character, although in Monochrome, the player’s model isn’t on screen. After this, it assigns points to the player depending on how accurate the game calculates they were and, if their HP isn’t full, increases it by a set amount and loops back to the play section. If the game determines that the user missed the note, a miss animation is queued and the miss counter at the bottom of the screen is increased by 1. The users HP is then reduced by a fixed amount. The game will next check if the player’s HP has dipped to 0, if so, the game ends and they are brought to a retry menu, if not, it loops back to the play section.

### JUMPSCARE EVENT
	This process happens when the countdown reaches set times throughout the song. When this happens, a translucent image of Gold’s face is transposed over the user’s gameplay for a short amount of time, accompanied by a sound effect, before it disappears and the process ends.

### CELEBI EVENT
	This event is also scripted to happen when the in-game timer reaches certain timestamps. This event happens exactly 3 time. When triggered, an animation of the Pokémon Celebi emerging from the dark background will play with subtitles “I’m dead” that will appear at the bottom of the screen. When this happens, the user’s max health will permanently be reduced by 20%, stacking each time for a grand total of a 60% max hp loss by the third trigger of the event. Following this, the process will end and return to the Play state.

### TYPING EVENT
	This is a scripted event that takes place at certain time intervals. When the event is active, a red screen appears with a word spelt out in a hard to read font. An invisible timer starts counting down. The player will then retype the word displayed. Failure to do so within the timer’s given time will cause the game to play an animation then move the user to the retry menu, else the process will redirect the player back to Play.

### PHASE2 EVENT
	This Event happens once and is scripted. Once the event starts, it plays a 10 second long animation where Gold’s head is pulled off his shoulders. Subtext “No More” is displayed and then all of Golds animations are updated to new ones to display his new state.


[Flowchart](images/Monochrome%20flowchart.jpg "Monochrome Flowchart")

## Class Diagram

>Explain your class Diagram

[Class Diagram](images/Monochrome%20Class%20Diagram.jpg "Monochrome Class Diagram")  

## Sequence Diagram

>Explain your class Diagram

[Sequence Diagram](images/Sequence%20diagram%20Monochrome.jpeg "Monochrome Sequence Diagram")  

## Other Resources

>If you have any other resources you want to add, like images, or links to other resources across the web please feel free to add them.

`Link your Images diagram here`  

## Github

- Github link for your repositor here  
