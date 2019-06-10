# Development of a ML-based Jet Tagger

User wants to gather some training data from an experiment so they can repeatedly run different ML training algorithms over it. Perhaps the sequence of operations:

 1. Analyzer wants to train a keras like deep/learning NN on jets. Each line of training data represents data associated with a jet. The goal is regression: measure the decay position in the calorimeter where a neutral long lived particle decays back into standard model particles (e.g. there will be a sudden deposit of energy).
 1. Analyzer decides on an initial list of variables. Say Jet pT, Eta, EMF, fraction of energy in each layer of the EM and HAD calorimeters.
 1. Analyzer Decides on initial datasets: 8 different MC datasets with signal.
 1. Analyzer makes input variable plots to inspect the inputs and make sure they are as expected.
 1. Analyzer runs quick training with simple network layout to make sure it "works", along with the actual decay position vs resulting. To get the initial version of the NN working it is likely they will have to inspect the text output of the tool - as it isn't hard to make a config mistake when setting up a training for the first time.
 1. Analyzer will want to run some hyper-parameter scans to understand what the limits of this NN are, and perhaps iterate over the network layout.
 1. Produce plots and tables with correlations good enough to show off to working group
 1. Go back and add jet width, as a result of a suggestion during the talk. And repeat the above sequence.
 1. Save the training and give it to someone else to run in the event processing workflow for the full analysis.
