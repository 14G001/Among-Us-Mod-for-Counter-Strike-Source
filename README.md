<img src="https://images.gamebanana.com/img/ss/tools/600bb714b68b9.jpg">

DESCRIPTION:<span class="GreenColor">&nbsp;</span><span class="GreenColor">it's a combination between TTT mode from Garry's Mod and Among Us game mode.</span><br><br>BLOG:&nbsp;<a href="https://forums.alliedmods.net/showthread.php?p=2733682" target="_blank">[CS:S] TTT (Among Us Version) 2021 (Trouble in Terrorist Town) - AlliedModders (alliedmods.net)</a><br><br><font size="4"><b><u><font color="Red">TTT (<font color="Lime">AMONG US</font>&nbsp;VERSION) FOR&nbsp;<font color="SeaGreen">Counter-Strike:Source</font>&nbsp;2021</font></u></b><br></font><br><br><font color="DarkOrange"><font size="3"><b><u>GAME MODE</u>&nbsp;(the following explanation is about the game mode that comes by default, it can be configured in a way that make the game mode change in certain aspects):</b></font><br><br></font><br><br><font size="3">Players can be&nbsp;<font color="Red">impostors</font>&nbsp;or&nbsp;<font color="DeepSkyBlue">innocents</font>. The majority of them will be&nbsp;<font color="DeepSkyBlue">innocents</font>.&nbsp;<font color="Red">Impostors</font>&nbsp;will have to kill a certain amount of hostages (that will spawn in random map positions in each round) before round time end to win.&nbsp;<font color="DeepSkyBlue">Innocents</font>&nbsp;will have to prevent this protecting hostages all time and trying to discover who is an&nbsp;<font color="Red">impostor</font>&nbsp;through the actions that the other players likely do.<br>Nobody knows who the&nbsp;<font color="red">impostors</font>&nbsp;are exempt from themselves (that will be able to check who are his teammates using the&nbsp;<u>!impostors</u>&nbsp;command, that will be censored in the chat on being written to make the other players be unable to see that wrote that), so that the&nbsp;<font color="DeepSkyBlue">innocents</font>&nbsp;can discover who the&nbsp;<font color="Red">impostors</font>&nbsp;are they will have to be attentive to what other players do. if a player acts in a suspicious way the alive&nbsp;<font color="DeepSkyBlue">innocents</font>&nbsp;will be able to tell all players what occurred and&nbsp;<font color="Red">impostors</font>&nbsp;will be able to defend themselves saying that thay weren't&nbsp;<font color="red">impostors</font>, killing the&nbsp;<font color="DeepSkyBlue">innocent</font>&nbsp;or scaping to kill the hostage before the&nbsp;<font color="deepskyblue">innocents</font>&nbsp;can prevent it.<br><font color="Red">Impostors</font>&nbsp;will be every round different players and assigned in a random way, but the amount of&nbsp;<font color="red">impostors</font>&nbsp;will be allways the same if the number of players never change (unless plugin has been confgured in a way that the amount of&nbsp;<font color="red">impostors</font>&nbsp;be random).</font><br><br><font size="3"><b>IMPORTANT: You will have to add the following convars to the server.cfg file (or better to the map config file if you have a map configs plugin like the following:&nbsp;<a href="https://forums.alliedmods.net/showthread.php?p=607079" target="_blank" rel="noopener">https://forums.alliedmods.net/showthread.php?p=607079</a>): "mp_friendlyfire 1", "mp_autokick 0", "mp_tkpunish 0", "mp_hostagepenalty 0", "mp_ignore_round_win_conditions 1".</b></font><br><br><font color="darkorange"><font size="3"><b><u>PLUGIN INCLUDES:</u></b></font><br><br></font><font size="2"><br>-Capacity to&nbsp;<b>configure the&nbsp;<font color="DeepSkyBlue">health of the hostages, number of hostages on the map</font></b>&nbsp;(can be any number),&nbsp;<b><font color="DeepSkyBlue">number of hostages that must be killed by the impostors and number of impostors depending on the number of players in the game</font></b>&nbsp;from the following text file: "cstrike/addons/sourcemod/configs/ttt/ttt_configs_per_player_quantity.txt". For example: From 0 to 4 players there are 2 impostors, 3 hostages and the hostages have 150 health, from 5 to 8 the hostages have 200 health, there are 3 impostors, . . .<br><br>-<b><font color="deepskyblue">Coordinates where the hostages can spawn</font>&nbsp;on the maps in text files</b>&nbsp;(modifiable, capacity to add up to 125 hostage spawns and if the plugin code is recompiled by modifying only one variable, even more spawns than 125 can be added) at the adress:<br>"cstrike/addons/sourcemod/configs/ttt/hostage_spawnpoints/<map_name>.txt".<br>To add coordinates write cl_showpos 1 in the game console and copy the values.<br>To remove them simply remove the coordinate from the text file (which would represent a line of it) IMPORTANT: Don't add a hostage spawn in the same place where there is a player spawn (T or CT) that could obstruct the spawn because otherwise It will crash the server or break when spawning a player in that position (MORE DETAILED EXPLANATION OF HOW TO ADD HOSTAGE SPAWNS BELOW).<br><br>-<b>Up to 32 different&nbsp;<font color="Lime">P</font><font color="Cyan">L</font><font color="Red">A</font><font color="Yellow">Y</font><font color="SandyBrown">E</font><font color="Blue">R</font>&nbsp;<font color="Orange">C</font><font color="SeaGreen">O</font><font color="Sienna">L</font><font color="Magenta">O</font><font color="Silver">R</font><font color="DarkOrchid">S</font></b>&nbsp;to be able to easily identify the players that are assigned automatically and can't be repeated in the players unless the number of players on the server at that time is more than 32 players (but the color can't repeat more than two times).<br><br>-Capacity for making&nbsp;<b>dead players talk to each other&nbsp;<font color="deepskyblue">without the alive players seeing what they write</font></b>&nbsp;(when they die, they will not be able to talk through the microphone with other players either) (If the sm_ttt_dead_players_mute command value is 1, it is 1 by default).<br><br>-Capacity to&nbsp;<b>change the&nbsp;<font color="deepskyblue">way of randomization to choose impostors</font></b>&nbsp;(allow there to be an impostor that was in the previous round or not, random amount of impostors or not, etc).<br><br>-<b><u><font color="Orange">SPECIAL AUTO-BAN SYSTEM</font></u>&nbsp;to prevent players from playing badly when there are no admins on server</b>, configurable and deactivatable (with the following commands: sm_ttt_ban_innocent_hostage_hurt, sm_ttt_ban_impostor_hurt_impostor, sm_ttt_ban_innocent_hurt_innocent, sm_ttt_ban_time).<br><br>-<b>Capacity to make alive players&nbsp;<font color="DeepSkyBlue">unable to hear shots of other players</font></b>&nbsp;so that it is more difficult for the innocent to discover the impostors (by default it is disabled so by default players can hear other players shots) (with the command sm_ttt_weapon_sounds).<br><br>-<b><font color="deepskyblue">Special chat from which only the impostors can communicate</font>&nbsp;to plan who they will kill</b>&nbsp;(sm_ttt_impostors_only_chat).<br><br>-Techniques to&nbsp;<b>prevent players from&nbsp;<font color="deepskyblue">seeing the minimap</font>, see&nbsp;<font color="deepskyblue">which players are alive or dead</font></b>&nbsp;(when using tab to see the scores),&nbsp;<b>which players die, etc</b>&nbsp;(unless they witness the act with their own user).<br><br>-<b>Players can see the&nbsp;<font color="deepskyblue">number of impostors at the beginning of the round, number of hostages at the beginning of the round, number of hostages health, number of hostages that must be eliminated for the impostors to win, number of players there start the game</font>, etc. with the&nbsp;<u>!info</u>&nbsp;command</b>&nbsp;(You can prevent them from seeing this if the sm_ttt_command_info command is changed to 0, by default it is 1).<br><br>-<b>Capacity to&nbsp;<font color="DeepSkyBlue">exclude admins from being banned or muted automatically</font></b>&nbsp;(with the sm_ttt_ban_admins and sm_ttt_mute_admins commands).<br><br>-Capacity to&nbsp;<b>make hostages always&nbsp;<font color="deepskyblue">spawn in random positions or always in the same ones</font></b>&nbsp;(everytime the number of players don't change in the second case) (with the sm_ttt_hostage_random_spawn command).<br><br>-Capacity to&nbsp;<b><font color="deepskyblue">check</font>&nbsp;if you are satisfied with the&nbsp;<font color="deepskyblue">hostages spawns</font>&nbsp;or you would like to modify them</b>&nbsp;(when using it, all the hostages will be spawned in all the positions that are in the hostage spawns configuration file), for this you have to use the command sm_ttt_show_every_hostage_spawn. When using it, all the hostages that may exist will always be spawned according to the configuration file with hostage spawns of the current map in game. To make it work, once the command is activated, the round must be finished to be able to see all the spawns (<u>THIS COMMAND WILL ONLY BE USEFUL WHEN THE SERVER IS CONFIGURING; IT IS NOT TO BE USED WHEN THE SERVER IS ONLINE</u>).<br><br>-<b>Command&nbsp;<u>!tttrules</u>&nbsp;that will&nbsp;<font color="deepskyblue">allow players who don't know the rules to see the rules</font></b>&nbsp;by writing it and the capacity to get a message from time to time that warns the player that it can be used (The repetition of the message is disabled if sm_ttt_rules_advice_repeat_time is 0, by default is 60). To change the settings this has to be done at the beginning of the round (it can be done with the map.cfg plugin surely).<br><br>-<b>Command&nbsp;<u>!impostors</u>&nbsp;that&nbsp;<font color="deepskyblue">allows impostors to see who the other impostors are</font></b>&nbsp;(it may work differently if the sm_ttt_command_imposters command wasn't 2).<br><br>-<b>Capacity to&nbsp;<font color="deepskyblue">modify the amount of money and score</font></b>&nbsp;(number of player kills that can be seen when using tab) that players get when winning the games.<br><br>-<b><font color="deepskyblue">Translations</font>&nbsp;until now</b>: in English and Spanish.<br><br>-<b><u><font color="deepskyblue">Maps with hostage spawn settings</font>&nbsp;that come with the plugin until now</u>: cs_assault, cs_compound, cs_italy, cs_militia, cs_office, cs_parkhouse, de_aztec, de_catalane_b6, de_chateau, de_dust, de_dust2, de_inferno, de_NewPortBeach, de_nightfever, de_nuke, de_piranesi, de_port, de_prodigy, de_rats_rc_1337v4, de_rush, de_season, de_thematrix_11, de_train, de_tropic_enhanced, de_wanda, de_westwood_2010, mg_smee_tower, mg_smee_tower_fix, mg_smee_tower_fix2, mg_tv_tower_v5, surf_buzzkill, surf_buzzkill2, surf_Swift.</b><br><br></map_name></font><br><br><font color="darkorange"><font size="3"><b><u>CONFIGURATION OF THE SPECIAL BAN SYSTEM:</u></b></font><br><br></font><br><font color="Lime"><b>BANNING FOR BEING AN INNOCENT AND HURTING INNOCENTS</b></font>&nbsp;(sm_ttt_ban_innocent_hurt_innocent): It works as follows: If the value of this command is 200 (very low value but I only use it for the example), an innocent person should kill 2 innocents or cause 200 damage to other innocents by being innocent to be banned. This is the only command that would make sense to disable because an innocent can't know if he's attacking an innocent or an imposter.<br><br><font color="lime"><b>BANNING FOR BEING AN IMPOSTOR AND HURTING IMPOSTORS</b></font>&nbsp;(sm_ttt_ban_impostor_hurt_impostor): It works the same as the previous one but for being an impostor and injuring or killing impostors. It isn't recommended to disable it because this would be most caused intentionally or by not knowing the rules.<br><br><font color="lime"><b>BANNING FOR BEING INNOCENT AND HURTING HOSTAGES</b></font>&nbsp;(sm_ttt_ban_innocent_hostage_hurt): If, for example, the value of the command is 8, an innocent would have to injure a hostage 8 times or kill 3 hostages to be banned. For every time an innocent kills a hostage he will be taken as if he had injured 3 hostages. It isn't recommended to disable it because this would be most caused intentionally or by not knowing the rules.<br><br><font color="lime"><b>BAT TIME IN MINUTES</b></font>&nbsp;(sm_ttt_ban_time): The value of this command will determine the number of minutes that a player will be banned when committing any of the actions mentioned before.<br><br>To&nbsp;<u>DISABLE THE AUTOMATIC BAN SYSTEM</u>&nbsp;OF THE MOD, leave the following convars at 0:<br>sm_ttt_ban_innocent_hostage_hurt, sm_ttt_ban_impostor_hurt_impostor, sm_ttt_ban_innocent_hurt_innocent.<br>IT IS NOT RECOMMENDED UNLESS THE SERVER ADMINS ARE ACTIVE, RELIABLE AND KNOW THE RULES, except for the sm_ttt_ban_innocent_hurt_innocent command that could be more logical than this at 0 due to the fact that innocents can't know if they are attacking an imposter or an innocent.<br><br><font color="darkorange"><font size="3"><b><u>CONFIGURATIONS PER NUMBER OF PLAYERS AND HOSTAGE SPAWNS:</u></b></font><br></font><br><br>To add or remove configurations per number of players (from 5 to 8 players there are 3 imposters for example, that type of configuration), you have to go to the following file: cstrike/addons/sourcemod/configs/ttt/ttt_configs_per_player_quantity.txt.<br><br>// FORMAT:<br><br>//| Number | Number |Number of hostages|Number of hostages| Hostage |<br>//| of | of | in the map at the | that must die | health |<br>//| players | impostors | beggining of the | for impostors | amount|<br>//| | | round | to win | |<br><br>//FROM 0 TO 4 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:<br>| 4 | 1 | 2 | 2 | 100 |<br>//FROM 5 TO 8 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:<br>| 8 | 1 | 4 | 2 | 200 |<br>//FROM 9 TO 11 PLAYERS THE FOLLOWING LINE WILL BE THE CONFIGS:<br>| 11 | 2 | 6 | 2 | 500 |<br>//THE SAME FOR ALL THE FOLLOWING LINES:<br>| 16 | 3 | 8 | 3 | 500 |<br>| 20 | 3 | 8 | 3 | 500 |<br>| 28 | 4 | 8 | 3 | 1000 |<br>| 36 | 4 | 8 | 3 | 500 |<br>| 42 | 5 | 8 | 3 | 500 |<br>// THE LAST LINE FROM 43 TO 65 PLAYERS (MAXIMUM OF CS:S).<br><br>// IS THE SAME IF YOU DO THE FOLLOWING:<br><br>4 1 2 2 100<br>8 1 4 2 200<br>11 2 6 2 500<br>16 3 8 3 500<br>20 3 8 3 500<br>28 4 8 3 1000<br>36 4 8 3 500<br>42 5 8 3 500<br><br>// ALWAYS THE VALUE OF Number Of Players HAS TO BE FROM LOWEST TO GREATEST ON // EACH LINE.<br><br>// IT IS IMPORTANT THAT THE NUMBERS ARE SEPARATED BY '|' O ' ' (SPACES). IF YOU TRY TO // SEPARATE THEM WITH ANOTHER TYPE OF CHARACTERS IT WILL NOT WORK AND YOU WILL // NOT BE ABLE TO PLAY WELL ON THE SERVER. IT IS IMPORTANT THAT EACH SETTING PER // NUMBER OF PLAYERS BE ON A DIFFERENT LINE.<br><br>// RESPECT TO THE FILE WITH THE COORDINATES IN WHICH THE HOSTAGES MAY SPAW, WHEN // ADDING THE VALUES, IT MUST BE DONE IN THE SAME WAY. TO WRITE TEXT OF ANY KIND IN // THE CONFIGURATION FILES, LIKE TO REMEMBER SOMETHING, YOU MUST DO THE // FOLLOWING: WRITE "//" AT THE BEGINNING OF THE TEXT LINE. THEN YOU CAN WRITE // ANYTHING. HOWEVER, TRY NOT TO WRITE TOO MANY CHARACTERS ON A SINGLE LINE.<br><br><font color="darkorange"><font size="3"><b><u>EDIT THE HOSTAGE SPAWNS CONFIGURATIONS:</u></b><br><br></font></font><br>Once we understand how the values will be written in the hostage spawns configuration file, we must know the following: If you want to make the configurations, you will have to do them for a specific map. To do this we will create a text file with the name of the map (for example, if you want to create a file with settings for de_dust2, the file must be called de_dust2.txt, and you will have to put it in the following address "cstrike/addons/sourcemod/configs/ttt/hostage_spawnpoints/<here goes="" the="" text="" file="" with="" map="" name="" class="SelectedElement"> ".<br><br>As the file is going to be empty we will have to look for the coordinates to add them to the file. To do that we will open the Counter-Strike: Source and once there we will create a game with the map for which we want to create the configurations. Once everything has loaded we will open the console in the game and type the following command there: cl_showpos 1 .<br><br>Once that is done, something like the following will appear on the screen in the upper right edge probably (if not elsewhere):<br><br>pos: 999.99 999.99 999.99<br>ang: 999.99 999.99 999.99<br>vel: 999.99<br><br>Once this appears, we must go to the position where we want the hostage to be spawn and for each spawn that we want to do, we must copy the pos and ang values in the position where the spawn will be and paste them into the text file that we created (all in the same line).<br>Let's imagine that what shows what came out after they typed the command cl_showpos 1 in the game console were variables, for example:<br><br>pos:&nbsp;<font color="Magenta">X1</font>&nbsp;<font color="Orange">Y1</font>&nbsp;<font color="Yellow">Z1</font><br>ang:&nbsp;<font color="Lime">X2</font>&nbsp;<font color="Cyan">Y2</font>&nbsp;<font color="DeepSkyBlue">Z2</font><br>vel: N<br><br>In the file that we created we should put:<br><br><font color="Magenta">X1</font>&nbsp;<font color="Orange">Y1</font>&nbsp;<font color="Yellow">Z1</font>&nbsp;<font color="Lime">X2</font>&nbsp;<font color="Cyan">Y2</font>&nbsp;<font color="DeepSkyBlue">Z2</font><br><br>In a different line for each new spawn. If the values were the following:<br><br>pos:&nbsp;<font color="Magenta">120</font>.22&nbsp;<font color="Orange">-243</font>.21&nbsp;<font color="Yellow">939</font>.32<br>ang:&nbsp;<font color="Lime">21</font>.33&nbsp;<font color="Cyan">-170</font>.34&nbsp;<font color="DeepSkyBlue">0</font><br>vel: N<br><br>And we would like to do a spawn in that coordinate, we would add the following to the file that we created for the map:<br><br><font color="Magenta">120</font>&nbsp;<font color="Orange">-243</font>&nbsp;<font color="Yellow">939</font>&nbsp;<font color="Lime">21</font>&nbsp;<font color="Cyan">-170</font>&nbsp;<font color="DeepSkyBlue">0</font><br><br>And for each coordinate we would do the same by adding them below the one written above.<br><br><font color="Magenta">120</font>&nbsp;<font color="Orange">-243</font>&nbsp;<font color="Yellow">939</font>&nbsp;<font color="Lime">21</font>&nbsp;<font color="Cyan">-170</font>&nbsp;<font color="DeepSkyBlue">0</font><br>-293 933 848 -32 122 0<br>328 -338 329 121 33 0<br>333 234 -1993 20 -173 29<br>324 -39 . . .<br>. . .<br><br><b>IMPORTANT:</b><br>-Keep in mind that REAL NUMBERS CANNOT BE ADDED, ONLY THE INTEGER PART.<br>-If we put a hostage spawn in a place where there's a T spawn, when spawning a T in that position, the server will crash due to an error. The same happens if it's a CT spawn. Make sure not to spawn positions where there are player spawns.<br><br>RECOMMENDATION: DO IT BY TAKING SCREENSHOTS, FOR EXAMPLE IN dust2 AND PASTING THEM ON Paint OR SOMETHING:&nbsp;<br><br><img src="https://screenshots.gamebanana.com/img/ss/tools/600cec69f340f.jpg"><br><br>AND THEN ADD ALL THE CONFIGURATIONS TO THE TEXT FILE (de_dust2.txt in this example).<br><br><font color="darkorange"><font size="3"><b><u>COMMANDS / CONVARS:</u></b><br></font></font><br><br><font color="DeepSkyBlue"><b>sm_ttt_overlay_impostors</b></font>&nbsp;= Path to overlay material file to show to impostors.<br>(Default: "overlays/ttt/impostors_overlay").<br><br><font color="deepskyblue"><b>sm_ttt_overlay_innocents</b></font>&nbsp;= Path to overlay material file to show to innocents.<br>(Default: "overlays/ttt/innocents_overlay").<br><br><font color="deepskyblue"><b>sm_ttt_min_player_quantity</b></font>&nbsp;= Minimum number of players to start the serious game. If it is 0 or less, the game starts with any number of players, even if they were very few (for example, it won't make sense to start the match with only 2 players in game). (Default: "4").<br><br><font color="deepskyblue"><b>sm_ttt_dead_players_mute</b></font>&nbsp;= If it is 1, the dead players CANNOT speak or write to alive players, only with other dead players, if it is 0, they can. (Default: "1").<br><br><font color="DeepSkyBlue"><b>sm_ttt_same_impostors</b></font>&nbsp;= If it is 1, the impostors can be the same as in the previous round. If it is 0 they can't. If it is 2, the number of impostors is random (always less than half the total number of players). (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_say_if_was_an_impostor</b></font>&nbsp;= Tell all players if the player who died was an imposter (If "1" tells, else don't). (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_ban_innocent_hostage_hurt</b></font>&nbsp;= Amount of times an innocent could injure a hostage until banned. If he kills him he counts as if he had hurt him 3 times. If it is 0 it is disabled).(Default: "11").<br><br><font color="deepskyblue"><b>sm_ttt_ban_impostor_hurt_impostor</b></font>&nbsp;= Amount of health that an impostor must take from an impostor to be banned (If it's 0 it's disabled). (Default: "300").<br><br><font color="deepskyblue"><b>sm_ttt_ban_innocent_hurt_innocent</b></font>&nbsp;= Amount of health that an innocent should take from another innocent to be banned. If it is 0 it is disabled. (Default: "700").<br><br><font color="deepskyblue"><b>sm_ttt_ban_time</b></font>&nbsp;= Number of minutes that a player will be banned in case of commenting on the indicated amount of inconsistencies. In case it is 0 the ban will be permanent. (Default: "20").<br><br><font color="deepskyblue"><b>sm_ttt_impostor_win_money</b></font>&nbsp;= Amount of money that will be assigned to impostors if they win. (Default: "4000").<br><br><font color="deepskyblue"><b>sm_ttt_innocent_win_money</b></font>&nbsp;= Amount of money that will be assigned to the innocent if they win. (Default: "2000").<br><br><font color="deepskyblue"><b>sm_ttt_impostor_win_points</b></font>&nbsp;= Amount of frags that will be assigned to impostors if they win. (Default: "3").<br><br><font color="deepskyblue"><b>sm_ttt_innocent_win_points</b></font>&nbsp;= Amount of frags that will be assigned to innocents if they win. (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_weapon_sounds</b></font>&nbsp;= Allows or not the alive players, to hear the shots of the other players or not. If it is 0 the alive players will only be able to hear their own shots. If it's 1, everyone can listen. (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_impostors_only_chat</b></font>&nbsp;= If enabled, imposters will be able to communicate with each other via team chat. (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_command_impostors</b></font>&nbsp;= If 0, only dead admins will be able to use this command. If 1, only dead players will be able to use this command. If 2, only impostors will be able to use this command. If 3, only impostors and dead players will be able to use this command. Dead admins will allways be able to use this command. (Default: "2").<br><br><font color="deepskyblue"><b>sm_ttt_command_info</b></font>&nbsp;= If 0 nobody will be able to use this command. If 1 everyone will be able to use it. (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_ban_admins</b></font>&nbsp;= If 0 admins won't be automatically banned in case they break the limits. (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_mute_admins</b></font>&nbsp;= If 0 admins won't be muted when they die. Admins will be able to use Team chat to communicate something to everybody. (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_hostage_random_spawn</b></font>&nbsp;= If 0, hostages allways spawn in the same positions. If 1 they spawn in rnadom positions. (Default: "1").<br><br><font color="deepskyblue"><b>sm_ttt_show_every_hostage_spawn</b></font>&nbsp;= THIS IS ONLY TO CHECK IF YOUR SPAWN CONFIGS ARE AS YOU IMAGINED IT OR IF YOU WANT TO MODIFY THEM. WHEN PLAYING WITH PEOPLE DISABLE IT. End round to see changes. To enable it 1 and to disable it and play normaly 0. (Default: "0").<br><br><font color="deepskyblue"><b>sm_ttt_rules_advice_repeat_time</b></font>&nbsp;= Time in seconds between rules message displays for all players. 0 to disable. (Default: "60").<br><br><font color="deepskyblue"><b>sm_ttt_scoreboard_player_alive_check</b></font>&nbsp;= Players can see if the other players are alive or not with the scoreboard. (Default: "0").<br><br><font size="3"><b>Enjoy!</b></font>&nbsp;<img src="https://forums.alliedmods.net/images/smilies/up.gif" border="0" alt="" title="Good" class="inlineimg"><br><br><font size="4"><b><u>INSTALLATION INSTRUCTIONS</u></b></font><br><br><font size="3">1- Download sm_ttt.zip file.<br><br><font size="3"><b>2- IMPORTANT: You will have to add the following convars to the server.cfg file (or better to the map config file if you have a map configs plugin like the following:&nbsp;<a href="https://forums.alliedmods.net/showthread.php?p=607079" target="_blank" rel="noopener">https://forums.alliedmods.net/showthread.php?p=607079</a>): "mp_friendlyfire 1", "mp_autokick 0", "mp_tkpunish 0", "mp_hostagepenalty 0", "mp_ignore_round_win_conditions 1".</b></font><br><br>3- Go to the cstrike folder on your server files and open it.<br><br>4- Once you are on the cstrike folder, open sm_ttt.zip file and copy and paste (or drag and drop) its files to the cstrike folder.<br><br>YOU WILL HAVE TO ADD MATERIALS FILES IN YOUR FTP SERVER.</font></here>