# #mafia - A good old-fashioned game of Mafia

Mafia is a game where townspeople, a doctor, and a sheriff fight against the Mafia,
a group of 1 or more people that can kill one player every turn.

Terminology:

 - *Narrator* - an operator of the channel, runs the game.
 - *Mafia* - One or more people; 1st to go, attacks one player.
 - *Doctor* - 2nd to go, can choose to save any living player.
 - *Sheriff* - Last to go, can choose 1 player to be executed as a Mafia member.

How a game works:

1. An operator gets a game together with 4 or more players and changes the topic to say that a game is in progress.
2. The operator, through some method (such as using a virtual deck of cards), assigns 1 Doctor, 1 Sheriff, and at least 1 Mafia (more than one can be used). Everybody else are Townspeople.
3. Mafia, as a game, functions on secrecy. Every player that has a move moves by private message with the Narrator.
4. All mafia players message the Narrator with the nick of 1 player.
5. If all of the Mafia chose the same person, the Narrator lets them know as such ("The mafia have reached consensus."). If not, each member of the mafia is told where the split is ("Three Mafia members chose joesmith, and one Mafia member chose jamescamp."), and the Narrator goes back to step 4.
6. Once the mafia have selected one player, the Doctor messages the Narrator with their choice of player to save.
7. The Sheriff chooses one player they believe is in the Mafia.
8. If the Doctor chose the same person as the Mafia, the Narrator presents a story in the main channel where the targeted player is harmed but not killed. Otherwise, the Narrator presents a story in which the player dies.
9. If the player the Sheriff chose is dead, the turn is over and the Narrator returns the game to step 4. If not, continue to step 10.
10. The Narrator presents a story in which the person who was chosen by the Sheriff is hung. (If the Sheriff is dead, the townspeople "read their notes" and come to the conclusion of that player being in the mafia.)
11. If the Sheriff is dead and there are Mafia present, the Mafia win, and get a reward in whatever fashion the Narrator deems appropriate (tcoin, whatever). If all of the Mafia members are dead (whether or not the Sheriff is still alive), the townspeople win. If either side has won, the game is over. (Go to step 13 if that is the case.)
12. Go back to step 4 and repeat.
13. The Narrator removes the tag from the topic saying the game is in progress.

