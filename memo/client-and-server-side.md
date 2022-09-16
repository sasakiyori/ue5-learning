# Client Side And Server Side

## Ref
https://docs.unrealengine.com/5.0/en-US/unreal-engine-terminology

## Concept

### Player Controller
Case of multiplayer game has 3 players 👉 

Server has 3 player controller instances, every client only has its own instance.
| SERVER | CLIENT1 | CLIENT2 | CLIENT3 |
| :----: | :----:  | :----:  | :----:  |
| pctl1  | pctl1'  |         |         |
| pctl2  |         | pctl2'  |         |
| pctl3  |         |         | pctl3'  |


### Player State
Case of multiplayer game has 3 players 👉 

Server has 3 player state, every client has 3 server side's replica to sync with server side.
| SERVER | CLIENT1 | CLIENT2 | CLIENT3 |
| :----: | :----:  | :----:  | :----:  |
| player-state1 | player-state1-replica-sync | player-state1-replica-sync | player-state1-replica-sync |
| player-state2 | player-state2-replica-sync | player-state2-replica-sync | player-state2-replica-sync |
| player-state3 | player-state3-replica-sync | player-state3-replica-sync | player-state3-replica-sync |


### Game Mode
Case of multiplayer game has 3 players 👉 

Server has 1 game mode in each level, every client has 1 server side's replica.
| SERVER | CLIENT1 | CLIENT2 | CLIENT3 |
| :----: | :----:  | :----:  | :----:  |
| mode | mode-replica | mode-replica | mode-replica |


### Game State
Case of multiplayer game has 3 players 👉 

Server has 1 game state, every client has 1 local game state to sync with server side.
| SERVER | CLIENT1 | CLIENT2 | CLIENT3 |
| :----: | :----:  | :----:  | :----:  |
| game-state | game-state-local-sync | game-state-local-sync | game-state-local-sync |

