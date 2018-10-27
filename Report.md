## Model

The model uses 3 hidden layers with 64 nodes each. These layers are all Linear with Relu activation.
## Hyperparameters
The Hyperparameters used for the Learning are:
      
GAMMA = 0.99   

TAU = 1e-3       

LearnRate = 5e-4 

UPDATE_EVERY = 4

BUFFER_SIZE = int(1e5)  

BATCH_SIZE = 64   

Where UPDATE_EVERY, BUFFER_SIZE, are BATCH_SIZE are used for memory Replay. Each memory replay replays 64 randomly sampled past experiences out of the past 10^5 experiences. It is updated every 4 replays.

LearnRate is the learning step rate to update the neural network weights. Gamma is the discount factor applied to expected rewards. TAU affects the amount that target Q network is updated by.
## The Results
The Problem was solved in 414 episodes.
![](EpisodePlot.png)

## The Future

For a future improvement I would implement a priotitized experience replay.