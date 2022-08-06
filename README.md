# SequenceDetectingNeuron

#Description of seq_response_graphs:
#This program sets up an LIF neuron that is sequence selective temporally. 
#Currently it will give the maximum response for a reverse sequence and 
#both forward as well as any scrambled sequence will not give as amplified a response, allowing us
#to pick out the reverse sequence from the rest.
#A sequence of 4 is given for each of the cases. The sequence selecting threshold in this case is -0.04 mV.
#The connections are set up such that the first synapse is activated at the time value of the first spike, 
#second synapse is activated at the time value of the second spike and so on.

#Description of seqsynhandler_lif_neuron:
#This program creates a sequence detecting LIF neuron.
#We can see the shapes of the membrane potential produced by various kernels. 
#The connections are set up such that the first synapse receives a spike at 3s, second at 4s and third at 5s.
#The connections, kernel and seqDt can be varied to obtain different results. 
