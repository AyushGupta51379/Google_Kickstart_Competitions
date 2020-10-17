# Concept

### Best concept
#### Solved for Test Set 1, with S=2, meaning only 4 rooms

#### Code works perfectly well and gives us 12 points for the test set 1

#### Logic - limited possibilites for n=4 rooms, we covered them logically and got the score

##### Corner rooms are symmetric, this reduces the number of cases to consider

##### How to solve

For test set 1

1st: We know that it only has S=2, thus the rooms are at: (1,1), (2,1), (2,2), (2,3). Here, (2,2) is the center room. Everyone wants the center room, since one player has it, that player has already won as the access to other rooms has been cut for the other player.

Let's call Alma as PA (Player A) and Berthe as PB (Player B).

Since initially the players have rooms and they have painted their own rooms. We can ignore these rooms in calculation of score. Since, score = Rooms of PA - Rooms of PB, the difference will already cancel their inital rooms.

Scenario 1 - no room under construction: Both players have painted their own rooms. Thus, 2 rooms out of 4 rooms have been painted.

SubScenario 1 - both players have corner rooms initially - Both of these already painted rooms are corner rooms. Since, PA has 1st turn, she will jump to the center room, Rooms of PA += 1. Now, PB has her turn, but she can't move as the center is the access point for any of the other rooms, and center has already been occupied by PA. Then, PA will have her turn and jump to the unpainted corner room. Adding 1 more room to her collection. In the end, Rooms of PA after initial = 1+1 (center+corner) = 2. Rooms of PB after initial = 0. Score = 2-0 = 2.

SubScenario 2 - PA has center room, PB has corner room. PA will paint 1 corner room, whereas PB can't move. Thus, Score = 1-0 = 1.

SubScenario 3 - PB has corner room, PA has center room. PB will paint 1 corner room, whereas PA can't move. Thus, Score = 0-1 = -1.

Scenario 2 - Construction

Subscenario 1 - 2 out of 4 rooms blocked. Score = 0. Since no one can move.

Subscenario 2 - 1 out of 4 rooms blocked. If center room is blocked, Score = 0. If corner room is blocked - If initially PA has center room - Score = 1-0 = 1. If initially PB has center room - Score = 0-1 = -1. If initially PA has center room - Score = 1-0 = 1. If both players have corner rooms and 1 corner is blocked. PA will take the center, Score = 1-0 = 1.