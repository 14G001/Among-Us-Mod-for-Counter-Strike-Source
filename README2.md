[CENTER][IMG]https://screenshots.gamebanana.com/img/ss/tools/600bb714b68b9.jpg[/IMG][/CENTER]

[SIZE="3"]In-Game images here: [url]https://gamebanana.com/tools/6942[/url][/SIZE]
[SIZE="3"]GitHub repository: [url]https://github.com/14G001/TTT-Mod--Among-Us-Version--2021-for-Counter-Strike-Source[/url][/SIZE]



[SIZE="6"][CENTER][B][U][COLOR="Red"]TTT ([COLOR="Lime"]AMONG US[/COLOR] VERSION) FOR [COLOR="SeaGreen"]Counter-Strike:Source[/COLOR] 2021[/U][/B][/CENTER][/SIZE][/COLOR]


[COLOR="DarkOrange"][CENTER][SIZE="3"][B][U]GAME MODE[/U] (the following explanation is about the game mode that comes by default, it can be configured in a way that make the game mode change in certain aspects):[/B][/SIZE][/CENTER][/COLOR]


[SIZE="3"]Players can be [COLOR="Red"]impostors[/COLOR] or [COLOR="DeepSkyBlue"]innocents[/COLOR]. The majority of them will be [COLOR="DeepSkyBlue"]innocents[/COLOR]. [COLOR="Red"]Impostors[/COLOR] will have to kill a certain amount of hostages (that will spawn in random map positions in each round) before round time end to win. [COLOR="DeepSkyBlue"]Innocents[/COLOR] will have to prevent this protecting hostages all time and trying to discover who is an [COLOR="Red"]impostor[/COLOR] through the actions that the other players likely do.
Nobody knows who the [COLOR="red"]impostors[/COLOR] are exempt from themselves (that will be able to check who are his teammates using the [U]!impostors[/U] command, that will be censored in the chat on being written to make the other players be unable to see that wrote that), so that the [COLOR="DeepSkyBlue"]innocents[/COLOR] can discover who the [COLOR="Red"]impostors[/COLOR] are they will have to be attentive to what other players do. if a player acts in a suspicious way the alive [COLOR="DeepSkyBlue"]innocents[/COLOR] will be able to tell all players what occurred and [COLOR="Red"]impostors[/COLOR] will be able to defend themselves saying that thay weren't [COLOR="red"]impostors[/COLOR], killing the [COLOR="DeepSkyBlue"]innocent[/COLOR] or scaping to kill the hostage before the [COLOR="deepskyblue"]innocents[/COLOR] can prevent it.
[COLOR="Red"]Impostors[/COLOR] will be every round different players and assigned in a random way, but the amount of [COLOR="red"]impostors[/COLOR] will be allways the same if the number of players never change (unless plugin has been confgured in a way that the amount of [COLOR="red"]impostors[/COLOR] be random).[/SIZE]


[SIZE="3"][B]IMPORTANT: You will have to add the following convars to the server.cfg file (or better to the map config file if you have a map configs plugin like the following: [url]https://forums.alliedmods.net/showthread.php?p=607079[/url]): "mp_friendlyfire 1", "mp_autokick 0", "mp_tkpunish 0", "mp_hostagepenalty 0", "mp_ignore_round_win_conditions 1".[/B][/SIZE]





[COLOR="darkorange"][CENTER][SIZE="3"][B][U]PLUGIN INCLUDES:[/U][/B][/SIZE][/CENTER][/COLOR]

[SIZE="2"]
-Capacity to [B]configure the [COLOR="DeepSkyBlue"]health of the hostages, number of hostages on the map[/COLOR][/B] (can be any number), [B][COLOR="DeepSkyBlue"]number of hostages that must be killed by the impostors and number of impostors depending on the number of players in the game[/COLOR][/B] from the following text file: "cstrike/addons/sourcemod/configs/ttt/ttt_configs_per_player_quantity.txt". For example: From 0 to 4 players there are 2 impostors, 3 hostages and the hostages have 150 health, from 5 to 8 the hostages have 200 health, there are 3 impostors, . . .

-[B][COLOR="deepskyblue"]Coordinates where the hostages can spawn[/COLOR] on the maps in text files[/B] (modifiable, capacity to add up to 125 hostage spawns and if the plugin code is recompiled by modifying only one variable, even more spawns than 125 can be added) at the adress:
"cstrike/addons/sourcemod/configs/ttt/hostage_spawnpoints/<MAP_NAME>.txt".
To add coordinates write cl_showpos 1 in the game console and copy the values.
To remove them simply remove the coordinate from the text file (which would represent a line of it) IMPORTANT: Don't add a hostage spawn in the same place where there is a player spawn (T or CT) that could obstruct the spawn because otherwise It will crash the server or break when spawning a player in that position (MORE DETAILED EXPLANATION OF HOW TO ADD HOSTAGE SPAWNS BELOW).

-[B]Up to 32 different [COLOR="Lime"]P[/COLOR][COLOR="Cyan"]L[/COLOR][COLOR="Red"]A[/COLOR][COLOR="Yellow"]Y[/COLOR][COLOR="SandyBrown"]E[/COLOR][COLOR="Blue"]R[/COLOR] [COLOR="Orange"]C[/COLOR][COLOR="SeaGreen"]O[/COLOR][COLOR="Sienna"]L[/COLOR][COLOR="Magenta"]O[/COLOR][COLOR="Silver"]R[/COLOR][COLOR="DarkOrchid"]S[/COLOR][/B] to be able to easily identify the players that are assigned automatically and can't be repeated in the players unless the number of players on the server at that time is more than 32 players (but the color can't repeat more than two times).

-Capacity for making [B]dead players talk to each other [COLOR="deepskyblue"]without the alive players seeing what they write[/COLOR][/B] (when they die, they will not be able to talk through the microphone with other players either) (If the sm_ttt_dead_players_mute command value is 1, it is 1 by default).

-Capacity to [B]change the [COLOR="deepskyblue"]way of randomization to choose impostors[/COLOR][/B] (allow there to be an impostor that was in the previous round or not, random amount of impostors or not, etc).

-[B][U][COLOR="Orange"]SPECIAL AUTO-BAN SYSTEM[/COLOR][/U] to prevent players from playing badly when there are no admins on server[/B], configurable and deactivatable (with the following commands: sm_ttt_ban_innocent_hostage_hurt, sm_ttt_ban_impostor_hurt_impostor, sm_ttt_ban_innocent_hurt_innocent, sm_ttt_ban_time).

-[B]Capacity to make alive players [COLOR="DeepSkyBlue"]unable to hear shots of other players[/COLOR][/B] so that it is more difficult for the innocent to discover the impostors (by default it is disabled so by default players can hear other players shots) (with the command sm_ttt_weapon_sounds).

-[B][COLOR="deepskyblue"]Special chat from which only the impostors can communicate[/COLOR] to plan who they will kill[/B] (sm_ttt_impostors_only_chat).

-Techniques to [B]prevent players from [COLOR="deepskyblue"]seeing the minimap[/COLOR], see [COLOR="deepskyblue"]which players are alive or dead[/COLOR][/B] (when using tab to see the scores), [B]which players die, etc[/B] (unless they witness the act with their own user).

-[B]Players can see the [COLOR="deepskyblue"]number of impostors at the beginning of the round, number of hostages at the beginning of the round, number of hostages health, number of hostages that must be eliminated for the impostors to win, number of players there start the game[/COLOR], etc. with the [U]!info[/U] command[/B] (You can prevent them from seeing this if the sm_ttt_command_info command is changed to 0, by default it is 1).

-[B]Capacity to [COLOR="DeepSkyBlue"]exclude admins from being banned or muted automatically[/COLOR][/B] (with the sm_ttt_ban_admins and sm_ttt_mute_admins commands).

-Capacity to [B]make hostages always [COLOR="deepskyblue"]spawn in random positions or always in the same ones[/COLOR][/B] (everytime the number of players don't change in the second case) (with the sm_ttt_hostage_random_spawn command).

-Capacity to [B][COLOR="deepskyblue"]check[/COLOR] if you are satisfied with the [COLOR="deepskyblue"]hostages spawns[/COLOR] or you would like to modify them[/B] (when using it, all the hostages will be spawned in all the positions that are in the hostage spawns configuration file), for this you have to use the command sm_ttt_show_every_hostage_spawn. When using it, all the hostages that may exist will always be spawned according to the configuration file with hostage spawns of the current map in game. To make it work, once the command is activated, the round must be finished to be able to see all the spawns ([U]THIS COMMAND WILL ONLY BE USEFUL WHEN THE SERVER IS CONFIGURING; IT IS NOT TO BE USED WHEN THE SERVER IS ONLINE[/U]).

-[B]Command [U]!tttrules[/U] that will [COLOR="deepskyblue"]allow players who don't know the rules to see the rules[/COLOR][/B] by writing it and the capacity to get a message from time to time that warns the player that it can be used (The repetition of the message is disabled if sm_ttt_rules_advice_repeat_time is 0, by default is 60). To change the settings this has to be done at the beginning of the round (it can be done with the map.cfg plugin surely).

-[B]Command [U]!impostors[/U] that [COLOR="deepskyblue"]allows impostors to see who the other impostors are[/COLOR][/B] (it may work differently if the sm_ttt_command_imposters command wasn't 2).

-[B]Capacity to [COLOR="deepskyblue"]modify the amount of money and score[/COLOR][/B] (number of player kills that can be seen when using tab) that players get when winning the games.

-[B][COLOR="deepskyblue"]Translations[/COLOR] until now[/B]: in English and Spanish.

-[B][U][COLOR="deepskyblue"]Maps with hostage spawn settings[/COLOR] that come with the plugin until now[/U]: cs_assault, cs_compound, cs_italy, cs_militia, cs_office, cs_parkhouse, de_aztec, de_catalane_b6, de_chateau, de_dust, de_dust2, de_inferno, de_NewPortBeach, de_nightfever, de_nuke, de_piranesi, de_port, de_prodigy, de_rats_rc_1337v4, de_rush, de_season, de_thematrix_11, de_train, de_tropic_enhanced, de_wanda, de_westwood_2010, mg_smee_tower, mg_smee_tower_fix, mg_smee_tower_fix2, mg_tv_tower_v5, surf_buzzkill, surf_buzzkill2, surf_Swift.[/B]

[/SIZE]






[COLOR="darkorange"][CENTER][SIZE="3"][B][U]CONFIGURATION OF THE SPECIAL BAN SYSTEM:[/U][/B][/SIZE][/CENTER][/COLOR]


[COLOR="Lime"][B]BANNING FOR BEING AN INNOCENT AND HURTING INNOCENTS[/B][/COLOR] (sm_ttt_ban_innocent_hurt_innocent): It works as follows: If the value of this command is 200 (very low value but I only use it for the example), an innocent person should kill 2 innocents or cause 200 damage to other innocents by being innocent to be banned. This is the only command that would make sense to disable because an innocent can't know if he's attacking an innocent or an imposter.

[COLOR="lime"][B]BANNING FOR BEING AN IMPOSTOR AND HURTING IMPOSTORS[/B][/COLOR]  (sm_ttt_ban_impostor_hurt_impostor): It works the same as the previous one but for being an impostor and injuring or killing impostors. It isn't recommended to disable it because this would be most caused intentionally or by not knowing the rules.

[COLOR="lime"][B]BANNING FOR BEING INNOCENT AND HURTING HOSTAGES[/B][/COLOR] (sm_ttt_ban_innocent_hostage_hurt): If, for example, the value of the command is 8, an innocent would have to injure a hostage 8 times or kill 3 hostages to be banned. For every time an innocent kills a hostage he will be taken as if he had injured 3 hostages. It isn't recommended to disable it because this would be most caused intentionally or by not knowing the rules.

[COLOR="lime"][B]BAT TIME IN MINUTES[/B][/COLOR] (sm_ttt_ban_time): The value of this command will determine the number of minutes that a player will be banned when committing any of the actions mentioned before.

To [U]DISABLE THE AUTOMATIC BAN SYSTEM[/U] OF THE MOD, leave the following convars at 0:
sm_ttt_ban_innocent_hostage_hurt, sm_ttt_ban_impostor_hurt_impostor, sm_ttt_ban_innocent_hurt_innocent. 
IT IS NOT RECOMMENDED UNLESS THE SERVER ADMINS ARE ACTIVE, RELIABLE AND KNOW THE RULES, except for the sm_ttt_ban_innocent_hurt_innocent command that could be more logical than this at 0 due to the fact that innocents can't know if they are attacking an imposter or an innocent.






[COLOR="darkorange"][CENTER][SIZE="3"][B][U]CONFIGURATIONS PER NUMBER OF PLAYERS AND HOSTAGE SPAWNS:[/U][/B][/SIZE][/CENTER][/COLOR]


To add or remove configurations per number of players (from 5 to 8 players there are 3 imposters for example, that type of configuration), you have to go to the following file: cstrike/addons/sourcemod/configs/ttt/ttt_configs_per_player_quantity.txt.

// FORMAT:

//| Number  |   Number    |Number of hostages|Number of hostages| Hostage |
//|        of        |        of           |    in the map at the   |       that must die       |   health  |
//|   players  |  impostors |    beggining of the    |       for impostors       |  amount|
//|                    |                        |               round              |              to win               |                  |

//FROM 0 TO 4 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:
  |    4   	          |      1  	    |      	       2    	                |                2                        |   100    |
//FROM 5 TO 8 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:
  |    8               |      1   	    |       	       4    	                |               2     	             |   200     |
//FROM 9 TO 11 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:
  |   11             |      2  	    |      	       6    	                |               2     	             |   500     |
//THE SAME FOR ALL THE FOLLOWING LINES:
  |   16            |      3   	    |      	       8  	                |               3     	             |   500     |
  |   20            |      3   	    |      	       8   	                |               3      	             |   500     |
  |   28            |      4  	    |      	       8    	                |               3     	             |  1000    |
  |   36            |      4  	    |      	       8    	                |               3    	             |   500     |
  |   42            |      5 	    |      	       8      	                |               3     	             |   500     |
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

// ALWAYS THE VALUE OF Number Of Players HAS TO BE FROM LOWEST TO GREATEST ON        // EACH LINE.

// IT IS IMPORTANT THAT THE NUMBERS ARE SEPARATED BY '|' O ' ' (SPACES). IF YOU TRY TO     // SEPARATE THEM WITH ANOTHER TYPE OF CHARACTERS IT WILL NOT WORK AND YOU WILL  // NOT BE ABLE TO PLAY WELL ON THE SERVER. IT IS IMPORTANT THAT EACH SETTING PER           // NUMBER OF PLAYERS BE ON A DIFFERENT LINE.

// RESPECT TO THE FILE WITH THE COORDINATES IN WHICH THE HOSTAGES MAY SPAW, WHEN // ADDING THE VALUES, IT MUST BE DONE IN THE SAME WAY. TO WRITE TEXT OF ANY KIND IN // THE CONFIGURATION FILES, LIKE TO REMEMBER SOMETHING, YOU MUST DO THE 	             // FOLLOWING: WRITE "//" AT THE BEGINNING OF THE TEXT LINE. THEN YOU CAN WRITE            // ANYTHING. HOWEVER, TRY NOT TO WRITE TOO MANY CHARACTERS ON A SINGLE LINE.






[COLOR="darkorange"][SIZE="3"][CENTER][B][U]EDIT THE HOSTAGE SPAWNS CONFIGURATIONS:[/U][/B][/CENTER][/SIZE][/COLOR]


Once we understand how the values will be written in the hostage spawns configuration file, we must know the following: If you want to make the configurations, you will have to do them for a specific map. To do this we will create a text file with the name of the map (for example, if you want to create a file with settings for de_dust2, the file must be called de_dust2.txt, and you will have to put it in the following address "cstrike/addons/sourcemod/configs/ttt/hostage_spawnpoints/<HERE GOES THE TEXT FILE WITH THE MAP NAME> ".

As the file is going to be empty we will have to look for the coordinates to add them to the file. To do that we will open the Counter-Strike: Source and once there we will create a game with the map for which we want to create the configurations. Once everything has loaded we will open the console in the game and type the following command there: cl_showpos 1 .

Once that is done, something like the following will appear on the screen in the upper right edge probably (if not elsewhere):

pos:  999.99  999.99  999.99
ang:  999.99  999.99  999.99
vel:  999.99  

Once this appears, we must go to the position where we want the hostage to be spawn and for each spawn that we want to do, we must copy the pos and ang values in the position where the spawn will be and paste them into the text file that we created (all in the same line).
Let's imagine that what shows what came out after they typed the command cl_showpos 1 in the game console were variables, for example:

pos:  [COLOR="Magenta"]X1[/COLOR]  [COLOR="Orange"]Y1[/COLOR]  [COLOR="Yellow"]Z1[/COLOR]
ang:  [COLOR="Lime"]X2[/COLOR]  [COLOR="Cyan"]Y2[/COLOR]  [COLOR="DeepSkyBlue"]Z2[/COLOR]
vel:  N  

In the file that we created we should put:

[COLOR="Magenta"]X1[/COLOR]  [COLOR="Orange"]Y1[/COLOR]  [COLOR="Yellow"]Z1[/COLOR]  [COLOR="Lime"]X2[/COLOR]  [COLOR="Cyan"]Y2[/COLOR]  [COLOR="DeepSkyBlue"]Z2[/COLOR]

In a different line for each new spawn. If the values were the following:

pos:  [COLOR="Magenta"]120[/COLOR].22  [COLOR="Orange"]-243[/COLOR].21  [COLOR="Yellow"]939[/COLOR].32
ang:  [COLOR="Lime"]21[/COLOR].33  [COLOR="Cyan"]-170[/COLOR].34   [COLOR="DeepSkyBlue"]0[/COLOR]
vel:  N  

And we would like to do a spawn in that coordinate, we would add the following to the file that we created for the map:

[COLOR="Magenta"]120[/COLOR]  [COLOR="Orange"]-243[/COLOR]  [COLOR="Yellow"]939[/COLOR]  [COLOR="Lime"]21[/COLOR]  [COLOR="Cyan"]-170[/COLOR]  [COLOR="DeepSkyBlue"]0[/COLOR]

And for each coordinate we would do the same by adding them below the one written above.

[COLOR="Magenta"]120[/COLOR]  [COLOR="Orange"]-243[/COLOR]  [COLOR="Yellow"]939[/COLOR]  [COLOR="Lime"]21[/COLOR]  [COLOR="Cyan"]-170[/COLOR]  [COLOR="DeepSkyBlue"]0[/COLOR]
-293  933  848  -32  122  0
328  -338  329  121  33  0
333  234 -1993  20  -173 29
324  -39  . . .
. . .

[B]IMPORTANT: [/B]
-Keep in mind that REAL NUMBERS CANNOT BE ADDED, ONLY THE INTEGER PART.
-If we put a hostage spawn in a place where there's a T spawn, when spawning a T in that position, the server will crash due to an error. The same happens if it's a CT spawn. Make sure not to spawn positions where there are player spawns.

RECOMMENDATION: DO IT BY TAKING SCREENSHOTS, FOR EXAMPLE IN dust2 AND PASTING THEM ON Paint OR SOMETHING. 

[IMG]https://screenshots.gamebanana.com/img/ss/tools/600cec69f340f.jpg[/IMG]

AND THEN ADD ALL THE CONFIGURATIONS TO THE TEXT FILE (de_dust2.txt in this example).






[COLOR="darkorange"][SIZE="3"][CENTER][B][U]COMMANDS / CONVARS:[/U][/B][/CENTER][/SIZE][/COLOR]


[COLOR="DeepSkyBlue"][B]sm_ttt_overlay_impostors[/B][/COLOR] = Path to overlay material file to show to impostors. 
(Default: "overlays/ttt/impostors_overlay").

[COLOR="deepskyblue"][B]sm_ttt_overlay_innocents[/B][/COLOR] =  Path to overlay material file to show to innocents. 
(Default: "overlays/ttt/innocents_overlay").

[COLOR="deepskyblue"][B]sm_ttt_min_player_quantity[/B][/COLOR] = Minimum number of players to start the serious game. If it is 0 or less, the game starts with any number of players, even if they were very few (for example, it won't make sense to start the match with only 2 players in game). (Default: "4").

[COLOR="deepskyblue"][B]sm_ttt_dead_players_mute[/B][/COLOR] = If it is 1, the dead players CANNOT speak or write to alive players, only with other dead players, if it is 0, they can. (Default: "1").

[COLOR="DeepSkyBlue"][B]sm_ttt_same_impostors[/B][/COLOR] = If it is 1, the impostors can be the same as in the previous round. If it is 0 they can't. If it is 2, the number of impostors is random (always less than half the total number of players). (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_say_if_was_an_impostor[/B][/COLOR] = Tell all players if the player who died was an imposter (If "1" tells, else don't). (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_ban_innocent_hostage_hurt[/B][/COLOR] = Amount of times an innocent could injure a hostage until banned. If he kills him he counts as if he had hurt him 3 times. If it is 0 it is disabled).(Default: "11").

[COLOR="deepskyblue"][B]sm_ttt_ban_impostor_hurt_impostor[/B][/COLOR] = Amount of health that an impostor must take from an impostor to be banned (If it's 0 it's disabled). (Default: "300").

[COLOR="deepskyblue"][B]sm_ttt_ban_innocent_hurt_innocent[/B][/COLOR] = Amount of health that an innocent should take from another innocent to be banned. If it is 0 it is disabled. (Default: "700").

[COLOR="deepskyblue"][B]sm_ttt_ban_time[/B][/COLOR] = Number of minutes that a player will be banned in case of commenting on the indicated amount of inconsistencies. In case it is 0 the ban will be permanent. (Default: "20").

[COLOR="deepskyblue"][B]sm_ttt_impostor_win_money[/B][/COLOR] = Amount of money that will be assigned to impostors if they win. (Default: "4000").

[COLOR="deepskyblue"][B]sm_ttt_innocent_win_money[/B][/COLOR] = Amount of money that will be assigned to the innocent if they win. (Default: "2000").

[COLOR="deepskyblue"][B]sm_ttt_impostor_win_points[/B][/COLOR] = Amount of frags that will be assigned to impostors if they win. (Default: "3").

[COLOR="deepskyblue"][B]sm_ttt_innocent_win_points[/B][/COLOR] = Amount of frags that will be assigned to innocents if they win. (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_weapon_sounds[/B][/COLOR] = Allows or not the alive players, to hear the shots of the other players or not. If it is 0 the alive players will only be able to hear their own shots. If it's 1, everyone can listen. (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_impostors_only_chat[/B][/COLOR] = If enabled, imposters will be able to communicate with each other via team chat. (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_command_impostors[/B][/COLOR] = If 0, only dead admins will be able to use this command. If 1, only dead players will be able to use this command. If 2, only impostors will be able to use this command. If 3, only impostors and dead players will be able to use this command. Dead admins will allways be able to use this command. (Default: "2").

[COLOR="deepskyblue"][B]sm_ttt_command_info[/B][/COLOR] = If 0 nobody will be able to use this command. If 1 everyone will be able to use it. (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_ban_admins[/B][/COLOR] = If 0 admins won't be automatically banned in case they break the limits. (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_mute_admins[/B][/COLOR] = If 0 admins won't be muted when they die. Admins will be able to use Team chat to communicate something to everybody. (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_hostage_random_spawn[/B][/COLOR] = If 0, hostages allways spawn in the same positions. If 1 they spawn in rnadom positions. (Default: "1").

[COLOR="deepskyblue"][B]sm_ttt_show_every_hostage_spawn[/B][/COLOR] = THIS IS ONLY TO CHECK IF YOUR SPAWN CONFIGS ARE AS YOU IMAGINED IT OR IF YOU WANT TO MODIFY THEM. WHEN PLAYING WITH PEOPLE DISABLE IT. End round to see changes. To enable it 1 and to disable it and play normaly 0. (Default: "0").

[COLOR="deepskyblue"][B]sm_ttt_rules_advice_repeat_time[/B][/COLOR] = Time in seconds between rules message displays for all players. 0 to disable. (Default: "60").

[COLOR="deepskyblue"][B]sm_ttt_scoreboard_player_alive_check[/B][/COLOR] = Players can see if the other players are alive or not with the scoreboard. (Default: "0").




[SIZE="3"][B]Enjoy![/B][/SIZE] :up:




[SIZE="4"][CENTER][B][U]INSTALLATION INSTRUCTIONS[/U][/B][/CENTER][/SIZE]

[SIZE="3"]1- Download sm_ttt.zip file.

[SIZE="3"][B]2- IMPORTANT: You will have to add the following convars to the server.cfg file (or better to the map config file if you have a map configs plugin like the following: [url]https://forums.alliedmods.net/showthread.php?p=607079[/url]): "mp_friendlyfire 1", "mp_autokick 0", "mp_tkpunish 0", "mp_hostagepenalty 0", "mp_ignore_round_win_conditions 1".[/B][/SIZE]

3- Go to the cstrike folder on your server files and open it.

4- Once you are on the cstrike folder, open sm_ttt.zip file and copy and paste (or drag and drop) its files to the cstrike folder.

YOU WILL HAVE TO ADD MATERIALS FILES IN YOUR FTP SERVER.[/SIZE]
