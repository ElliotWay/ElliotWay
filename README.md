### Dr. Elliot E. Way

I'm currently between jobs. I finished my PhD in Computer Science in May 2022 at Binghamton University. My research was in Machine Learning, particularly Reinforcement Learning.

If you're here, you're probably looking for a code sample.

[RL_PDE](https://github.com/ElliotWay/RL_PDE) was a collaboration with GE on a DARPA grant that got me through the end of my PhD.
The idea was to learn to improve how PDEs are modeled with reinforcment learning.
My favorite pieces of code are:

* [RL_PDE/models/full.py](https://github.com/ElliotWay/RL_PDE/blob/master/models/full.py) - 
The idea that eventually worked was to encode an entire RL episode into a recurrent neural network.
But this recurrent network was unusual in that it didn't have inputs at each timestep, so we couldn't use the existing recurrent networks in Tensorflow.
Instead, I wrote a new recurrent network cell and the wrapping recurrent network from scratch in this file.

* [RL_PDE/param_sweep_template.py](https://github.com/ElliotWay/RL_PDE/blob/master/param_sweep_template.py) - 
Running different experiments with different parameters takes effort and is difficult to keep track of.
This script allows for starting experiments with many different parameters configurations at once.
There are existing alternative means of keeping track hyperparameters, but I ended up writing this one from scratch.
This script creates a process for every configuration, running N at a time depending on the number of processes set,
and printing lines of output from every process simultaneously, where lines are distinguished by a colored number for the process
e.g. "1: some output".
Among other things, this script keeps track of the Git hash and complains when it changes to prevent inconsistent experiments.
I needed things I learned in my Operating Systems class for this script.

If RL_PDE isn't enough, another project from before I started graduate school is [Guitar-Wizard](https://github.com/ElliotWay/Guitar-Wizard).
This is notable because it's the only code I have that wasn't part of research, and because I tried to create tests for everything in the test directory.
I haven't looked very closely at this since 2015, but I still think it was good code.
