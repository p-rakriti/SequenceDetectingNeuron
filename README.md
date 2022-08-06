# SequenceDetectingNeuron

Trying to answer the question of how the brain is able to detect whether an object is moving or
not, and how it is also able to predict where the moving object will reach after
a certain time. For example, we are able to declare that a ball thrown towards
us is moving because we understand that as time passes, the position of the ball
changes in space- its distance from the thrower increases monotonically. We are
also able to determine when and where the ball will reach, enabling us to catch
it.
In order to achieve this, neurons in the brain process movement in a particular
direction as a series of sequential inputs. As time passes, they perceive the
changing position of the movement as a sequence in space. Only if the (x+ 1)th
coordinate is reached after the xth coordinate is the object said to be moving
in a certain direction along the x direction. Correspondingly, only if the (x+ 1)th neuron
fires after the xth neuron is input deemed to be sequential.

Here it is done using the software MOOSE developed by Prof. Upinder Bhalla, NCBS - https://moose.ncbs.res.in/ .
SeqSynHandler is the class in MOOSE that handles sequential input.

An LIF neuron is assigned a kernel of the given form and is found to be sequence selective, or only a particular sequence causes the membrane potential to
cross the corresponding threshold. We can determine when the input is sequential based on when the membrane potential crosses the assigned threshold.


Description of seq_response_graphs:
This program sets up an LIF neuron that is sequence selective temporally. 
Currently it will give the maximum response for a reverse sequence and 
both forward as well as any scrambled sequence will not give as amplified a response, allowing us
to pick out the reverse sequence from the rest.
A sequence of 4 is given for each of the cases. The sequence selecting threshold in this case is -0.04 mV.
The connections are set up such that the first synapse is activated at the time value of the first spike, 
second synapse is activated at the time value of the second spike and so on.

Description of seqsynhandler_lif_neuron:
This program creates a sequence detecting LIF neuron.
We can see the shapes of the membrane potential produced by various kernels. 
The connections are set up such that the first synapse receives a spike at 3s, second at 4s and third at 5s.
The connections, kernel and seqDt can be varied to obtain different results. 
