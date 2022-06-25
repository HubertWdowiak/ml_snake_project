# Snake game using reinforcement learning with PyTorch and Pygame

In our project we used a ready python game and reinforcement learning solution which can be found here:
https://www.youtube.com/playlist?list=PLqnslRFeH2UrDh7vUmJ60YrmWd64mTTKV

As part of the project, we modified the program and added the following features:
- possibility to read and use an already trained model
- modified reinforcement learning algorithm (snake monitors area around him/monitors whole game board)
- added poissoned apples which should be dodged by the snake.

Previously the NN input-state was created as an eleven-element-list containing information about [current snake direction combined with information about possible colisions for each direction, current snake direction, current food position]. The algorithm upgrade used information about snake neighboring fields within a particular range (if there is a colision or not). 
The modified algorithm failed to learn how to play the game. We are not sure what is the reason for this. There are many learning features, so the final deep neural network is much more complex. We continued the learning process overnight, but could not achieve a score higher than 3. 

## Example learning processes of the model modified to observe its neighborhood:
<img width="624" alt="Zrzut ekranu 2022-06-12 o 14 23 01" src="https://user-images.githubusercontent.com/56223666/175788794-1d043316-ddce-46a1-b03b-546a524b8434.png">

## Example learning processes of the model modified to observe whole game board:
<img width="598" alt="Zrzut ekranu 2022-06-11 o 16 22 28" src="https://user-images.githubusercontent.com/56223666/175788789-fb9e7f0a-d64c-4b20-996b-0ef27bb009af.png">

On the other hand, the model has learned to avoid poisoned apples, and preloaded models are able to achieve high scores much earlier than those trained from scratch
