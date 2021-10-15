# TTT (AMONG US VERSION) FOR Counter-Strike: Source 2021 

<p align="center"> <img src="https://images.gamebanana.com/img/ss/tools/600bb714b68b9.jpg"> <p align="center">

- ### [In-Game images](https://gamebanana.com/tools/6942)
- ### [BLOG](https://forums.alliedmods.net/showthread.php?p=2733682/sm_ttt.sp)


### GAME MODE (the following explanation is about the game mode that comes by default, it can be configured in a way that make the game mode change in certain aspects):



Players can be impostors or innocents. The majority of them will be innocents. Impostors will have to kill a certain amount of hostages (that will spawn in random map positions in each round) before round time end to win. Innocents will have to prevent this protecting hostages all time and trying to discover who is an impostor through the actions that the other players likely do.
Nobody knows who the impostors are exempt from themselves (that will be able to check who are his teammates using the !impostors command, that will be censored in the chat on being written to make the other players be unable to see that wrote that), so that the innocents can discover who the impostors are they will have to be attentive to what other players do. if a player acts in a suspicious way the alive innocents will be able to tell all players what occurred and impostors will be able to defend themselves saying that thay weren't impostors, killing the innocent or scaping to kill the hostage before the innocents can prevent it.
Impostors will be every round different players and assigned in a random way, but the amount of impostors will be allways the same if the number of players never change (unless plugin has been confgured in a way that the amount of impostors be random).


#### IMPORTANT: You will have to add the following convars to the server.cfg file (or better to the map config file if you have a map configs plugin like the following: https://forums.alliedmods.net/showthread.php?p=607079): "mp_friendlyfire 1", "mp_autokick 0", "mp_tkpunish 0", "mp_hostagepenalty 0", "mp_ignore_round_win_conditions 1".



|

# PLUGIN INCLUDES:



- Capacity to configure the health of the hostages, number of hostages on the map (can be any number), number of hostages that must be killed by the impostors and number of impostors depending on the number of players in the game from the following text file: "cstrike/addons/sourcemod/configs/ttt/ttt_configs_per_player_quantity.txt". For example: From 0 to 4 players there are 2 impostors, 3 hostages and the hostages have 150 health, from 5 to 8 the hostages have 200 health, there are 3 impostors, . . .

- Coordinates where the hostages can spawn on the maps in text files (modifiable, capacity to add up to 125 hostage spawns and if the plugin code is recompiled by modifying only one variable, even more spawns than 125 can be added) at the adress:
"cstrike/addons/sourcemod/configs/ttt/hostage_spawnpoints/<MAP_NAME>.txt".
To add coordinates write cl_showpos 1 in the game console and copy the values.
To remove them simply remove the coordinate from the text file (which would represent a line of it) IMPORTANT: Don't add a hostage spawn in the same place where there is a player spawn (T or CT) that could obstruct the spawn because otherwise It will crash the server or break when spawning a player in that position (MORE DETAILED EXPLANATION OF HOW TO ADD HOSTAGE SPAWNS BELOW).

- Up to 32 different PLAYER COLORS to be able to easily identify the players that are assigned automatically and can't be repeated in the players unless the number of players on the server at that time is more than 32 players (but the color can't repeat more than two times).

- Capacity for making dead players talk to each other without the alive players seeing what they write (when they die, they will not be able to talk through the microphone with other players either) (If the sm_ttt_dead_players_mute command value is 1, it is 1 by default).

- Capacity to change the way of randomization to choose impostors (allow there to be an impostor that was in the previous round or not, random amount of impostors or not, etc).

- SPECIAL AUTO-BAN SYSTEM to prevent players from playing badly when there are no admins on server, configurable and deactivatable (with the following commands: sm_ttt_ban_innocent_hostage_hurt, sm_ttt_ban_impostor_hurt_impostor, sm_ttt_ban_innocent_hurt_innocent, sm_ttt_ban_time).

- Capacity to make alive players unable to hear shots of other players so that it is more difficult for the innocent to discover the impostors (by default it is disabled so by default players can hear other players shots) (with the command sm_ttt_weapon_sounds).

- Special chat from which only the impostors can communicate to plan who they will kill (sm_ttt_impostors_only_chat).

- Techniques to prevent players from seeing the minimap, see which players are alive or dead (when using tab to see the scores), which players die, etc (unless they witness the act with their own user).

- Players can see the number of impostors at the beginning of the round, number of hostages at the beginning of the round, number of hostages health, number of hostages that must be eliminated for the impostors to win, number of players there start the game, etc. with the !info command (You can prevent them from seeing this if the sm_ttt_command_info command is changed to 0, by default it is 1).

- Capacity to exclude admins from being banned or muted automatically (with the sm_ttt_ban_admins and sm_ttt_mute_admins commands).

- Capacity to make hostages always spawn in random positions or always in the same ones (everytime the number of players don't change in the second case) (with the sm_ttt_hostage_random_spawn command).

- Capacity to check if you are satisfied with the hostages spawns or you would like to modify them (when using it, all the hostages will be spawned in all the positions that are in the hostage spawns configuration file), for this you have to use the command sm_ttt_show_every_hostage_spawn. When using it, all the hostages that may exist will always be spawned according to the configuration file with hostage spawns of the current map in game. To make it work, once the command is activated, the round must be finished to be able to see all the spawns (THIS COMMAND WILL ONLY BE USEFUL WHEN THE SERVER IS CONFIGURING; IT IS NOT TO BE USED WHEN THE SERVER IS ONLINE).

- Command !tttrules that will allow players who don't know the rules to see the rules by writing it and the capacity to get a message from time to time that warns the player that it can be used (The repetition of the message is disabled if sm_ttt_rules_advice_repeat_time is 0, by default is 60). To change the settings this has to be done at the beginning of the round (it can be done with the map.cfg plugin surely).

- Command !impostors that allows impostors to see who the other impostors are (it may work differently if the sm_ttt_command_imposters command wasn't 2).

- Capacity to modify the amount of money and score (number of player kills that can be seen when using tab) that players get when winning the games.

- Translations until now: in English and Spanish.

- Maps with hostage spawn settings that come with the plugin until now: cs_assault, cs_compound, cs_italy, cs_militia, cs_office, cs_parkhouse, de_aztec, de_catalane_b6, de_chateau, de_dust, de_dust2, de_inferno, de_NewPortBeach, de_nightfever, de_nuke, de_piranesi, de_port, de_prodigy, de_rats_rc_1337v4, de_rush, de_season, de_thematrix_11, de_train, de_tropic_enhanced, de_wanda, de_westwood_2010, mg_smee_tower, mg_smee_tower_fix, mg_smee_tower_fix2, mg_tv_tower_v5, surf_buzzkill, surf_buzzkill2, surf_Swift.


|

## CONFIGURATION OF THE SPECIAL BAN SYSTEM:


### -BANNING FOR BEING AN INNOCENT AND HURTING INNOCENTS (sm_ttt_ban_innocent_hurt_innocent):
It works as follows: If the value of this command is 200 (very low value but I only use it for the example), an innocent person should kill 2 innocents or cause 200 damage to other innocents by being innocent to be banned. This is the only command that would make sense to disable because an innocent can't know if he's attacking an innocent or an imposter.

### -BANNING FOR BEING AN IMPOSTOR AND HURTING IMPOSTORS
(sm_ttt_ban_impostor_hurt_impostor): It works the same as the previous one but for being an impostor and injuring or killing impostors. It isn't recommended to disable it because this would be most caused intentionally or by not knowing the rules.

### -BANNING FOR BEING INNOCENT AND HURTING HOSTAGES
(sm_ttt_ban_innocent_hostage_hurt): If, for example, the value of the command is 8, an innocent would have to injure a hostage 8 times or kill 3 hostages to be banned. For every time an innocent kills a hostage he will be taken as if he had injured 3 hostages. It isn't recommended to disable it because this would be most caused intentionally or by not knowing the rules.

### -BAN TIME IN MINUTES (sm_ttt_ban_time): The value of this command will determine the number of minutes that a player will be banned when committing any of the actions mentioned before.

To DISABLE THE AUTOMATIC BAN SYSTEM OF THE MOD, leave the following convars at 0:
sm_ttt_ban_innocent_hostage_hurt, sm_ttt_ban_impostor_hurt_impostor, sm_ttt_ban_innocent_hurt_innocent.
IT IS NOT RECOMMENDED UNLESS THE SERVER ADMINS ARE ACTIVE, RELIABLE AND KNOW THE RULES, except for the sm_ttt_ban_innocent_hurt_innocent command that could be more logical than this at 0 due to the fact that innocents can't know if they are attacking an imposter or an innocent.

|

## CONFIGURATIONS PER NUMBER OF PLAYERS AND HOSTAGE SPAWNS:


To add or remove configurations per number of players (from 5 to 8 players there are 3 imposters for example, that type of configuration), you have to go to the following file: cstrike/addons/sourcemod/configs/ttt/ttt_configs_per_player_quantity.txt.

// FORMAT:

//| Number | Number |Number of hostages|Number of hostages| Hostage |
//| of | of | in the map at the | that must die | health |
//| players | impostors | beggining of the | for impostors | amount|
//| | | round | to win | |

//FROM 0 TO 4 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:
| 4 | 1 | 2 | 2 | 100 |
//FROM 5 TO 8 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:
| 8 | 1 | 4 | 2 | 200 |
//FROM 9 TO 11 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:
| 11 | 2 | 6 | 2 | 500 |
//THE SAME FOR ALL THE FOLLOWING LINES:
| 16 | 3 | 8 | 3 | 500 |
| 20 | 3 | 8 | 3 | 500 |
| 28 | 4 | 8 | 3 | 1000 |
| 36 | 4 | 8 | 3 | 500 |
| 42 | 5 | 8 | 3 | 500 |
// THE LAST LINE FROM 43 TO 65 PLAYERS (MAXIMUM OF CS:S).

// IS THE SAME IF YOU DO THE FOLLOWING:

4 1 2 2 100
8 1 4 2 200
11 2 6 2 500
16 3 8 3 500
20 3 8 3 500
28 4 8 3 1000
36 4 8 3 500
42 5 8 3 500

// ALWAYS THE VALUE OF Number Of Players HAS TO BE FROM LOWEST TO GREATEST ON // EACH LINE.

// IT IS IMPORTANT THAT THE NUMBERS ARE SEPARATED BY '|' O ' ' (SPACES). IF YOU TRY TO // SEPARATE THEM WITH ANOTHER TYPE OF CHARACTERS IT WILL NOT WORK AND YOU WILL // NOT BE ABLE TO PLAY WELL ON THE SERVER. IT IS IMPORTANT THAT EACH SETTING PER // NUMBER OF PLAYERS BE ON A DIFFERENT LINE.

// RESPECT TO THE FILE WITH THE COORDINATES IN WHICH THE HOSTAGES MAY SPAW, WHEN // ADDING THE VALUES, IT MUST BE DONE IN THE SAME WAY. TO WRITE TEXT OF ANY KIND IN // THE CONFIGURATION FILES, LIKE TO REMEMBER SOMETHING, YOU MUST DO THE // FOLLOWING: WRITE "//" AT THE BEGINNING OF THE TEXT LINE. THEN YOU CAN WRITE // ANYTHING. HOWEVER, TRY NOT TO WRITE TOO MANY CHARACTERS ON A SINGLE LINE.



|

## EDIT THE HOSTAGE SPAWNS CONFIGURATIONS:



Once we understand how the values will be written in the hostage spawns configuration file, we must know the following: If you want to make the configurations, you will have to do them for a specific map. To do this we will create a text file with the name of the map (for example, if you want to create a file with settings for de_dust2, the file must be called de_dust2.txt, and you will have to put it in the following address "cstrike/addons/sourcemod/configs/ttt/hostage_spawnpoints/<HERE GOES THE TEXT FILE WITH THE MAP NAME> ".

As the file is going to be empty we will have to look for the coordinates to add them to the file. To do that we will open the Counter-Strike: Source and once there we will create a game with the map for which we want to create the configurations. Once everything has loaded we will open the console in the game and type the following command there: cl_showpos 1 .

Once that is done, something like the following will appear on the screen in the upper right edge probably (if not elsewhere):

pos: 999.99 999.99 999.99
ang: 999.99 999.99 999.99
vel: 999.99

Once this appears, we must go to the position where we want the hostage to be spawn and for each spawn that we want to do, we must copy the pos and ang values in the position where the spawn will be and paste them into the text file that we created (all in the same line).
Let's imagine that what shows what came out after they typed the command cl_showpos 1 in the game console were variables, for example:

pos: X1 Y1 Z1
ang: X2 Y2 Z2
vel: N

In the file that we created we should put:

X1 Y1 Z1 X2 Y2 Z2

In a different line for each new spawn. If the values were the following:

pos: 120.22 -243.21 939.32
ang: 21.33 -170.34 0
vel: N

And we would like to do a spawn in that coordinate, we would add the following to the file that we created for the map:

120 -243 939 21 -170 0

And for each coordinate we would do the same by adding them below the one written above.

120 -243 939 21 -170 0
-293 933 848 -32 122 0
328 -338 329 121 33 0
333 234 -1993 20 -173 29
324 -39 . . .
. . .

### IMPORTANT:
-Keep in mind that REAL NUMBERS CANNOT BE ADDED, ONLY THE INTEGER PART.
-If we put a hostage spawn in a place where there's a T spawn, when spawning a T in that position, the server will crash due to an error. The same happens if it's a CT spawn. Make sure not to spawn positions where there are player spawns.

RECOMMENDATION: DO IT BY TAKING SCREENSHOTS, FOR EXAMPLE IN dust2 AND PASTING THEM ON Paint OR SOMETHING.

<img src="https://screenshots.gamebanana.com/img/ss/tools/600cec69f340f.jpg">

AND THEN ADD ALL THE CONFIGURATIONS TO THE TEXT FILE (de_dust2.txt in this example).


# COMMANDS / CONVARS:

- sm_ttt_overlay_impostors = Path to overlay material file to show to impostors.
(Default: "overlays/ttt/impostors_overlay").

- sm_ttt_overlay_innocents = Path to overlay material file to show to innocents.
(Default: "overlays/ttt/innocents_overlay").

- sm_ttt_min_player_quantity = Minimum number of players to start the serious game. If it is 0 or less, the game starts with any number of players, even if they were very few (for example, it won't make sense to start the match with only 2 players in game). (Default: "4").

- sm_ttt_dead_players_mute = If it is 1, the dead players CANNOT speak or write to alive players, only with other dead players, if it is 0, they can. (Default: "1").

- sm_ttt_same_impostors = If it is 1, the impostors can be the same as in the previous round. If it is 0 they can't. If it is 2, the number of impostors is random (always less than half the total number of players). (Default: "1").

- sm_ttt_say_if_was_an_impostor = Tell all players if the player who died was an imposter (If "1" tells, else don't). (Default: "1").

- sm_ttt_ban_innocent_hostage_hurt = Amount of times an innocent could injure a hostage until banned. If he kills him he counts as if he had hurt him 3 times. If it is 0 it is disabled).(Default: "11").

- sm_ttt_ban_impostor_hurt_impostor = Amount of health that an impostor must take from an impostor to be banned (If it's 0 it's disabled). (Default: "300").

- sm_ttt_ban_innocent_hurt_innocent = Amount of health that an innocent should take from another innocent to be banned. If it is 0 it is disabled. (Default: "700").

- sm_ttt_ban_time = Number of minutes that a player will be banned in case of commenting on the indicated amount of inconsistencies. In case it is 0 the ban will be permanent. (Default: "20").

- sm_ttt_impostor_win_money = Amount of money that will be assigned to impostors if they win. (Default: "4000").

- sm_ttt_innocent_win_money = Amount of money that will be assigned to the innocent if they win. (Default: "2000").

- sm_ttt_impostor_win_points = Amount of frags that will be assigned to impostors if they win. (Default: "3").

- sm_ttt_innocent_win_points = Amount of frags that will be assigned to innocents if they win. (Default: "1").

- sm_ttt_weapon_sounds = Allows or not the alive players, to hear the shots of the other players or not. If it is 0 the alive players will only be able to hear their own shots. If it's 1, everyone can listen. (Default: "1").

- sm_ttt_impostors_only_chat = If enabled, imposters will be able to communicate with each other via team chat. (Default: "1").

- sm_ttt_command_impostors = If 0, only dead admins will be able to use this command. If 1, only dead players will be able to use this command. If 2, only impostors will be able to use this command. If 3, only impostors and dead players will be able to use this command. Dead admins will allways be able to use this command. (Default: "2").

- sm_ttt_command_info = If 0 nobody will be able to use this command. If 1 everyone will be able to use it. (Default: "1").

- sm_ttt_ban_admins = If 0 admins won't be automatically banned in case they break the limits. (Default: "1").

- sm_ttt_mute_admins = If 0 admins won't be muted when they die. Admins will be able to use Team chat to communicate something to everybody. (Default: "1").

- sm_ttt_hostage_random_spawn = If 0, hostages allways spawn in the same positions. If 1 they spawn in rnadom positions. (Default: "1").

- sm_ttt_show_every_hostage_spawn = THIS IS ONLY TO CHECK IF YOUR SPAWN CONFIGS ARE AS YOU IMAGINED IT OR IF YOU WANT TO MODIFY THEM. WHEN PLAYING WITH PEOPLE DISABLE IT. End round to see changes. To enable it 1 and to disable it and play normaly 0. (Default: "0").

- sm_ttt_rules_advice_repeat_time = Time in seconds between rules message displays for all players. 0 to disable. (Default: "60").

- sm_ttt_scoreboard_player_alive_check = Players can see if the other players are alive or not with the scoreboard. (Default: "0").



|



### INSTALLATION INSTRUCTIONS


1- Download sm_ttt.zip file.

2- IMPORTANT: You will have to add the following convars to the server.cfg file (or better to the map config file if you have a map configs plugin like the following: https://forums.alliedmods.net/showthread.php?p=607079): "mp_friendlyfire 1", "mp_autokick 0", "mp_tkpunish 0", "mp_hostagepenalty 0", "mp_ignore_round_win_conditions 1".

3- Go to the cstrike folder on your server files and open it.

4- Once you are on the cstrike folder, open sm_ttt.zip file and copy and paste (or drag and drop) its files to the cstrike folder.

### YOU WILL HAVE TO ADD MATERIALS FILES IN YOUR FTP SERVER.

## Enjoy! :D
