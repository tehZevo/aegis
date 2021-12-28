# Aegis Project

## What is it?
The Aegis Project (or just "Aegis") is an exploration of combining reinforcement learning, transfer learning, microservices, and automation concepts.
At its core, it provides standard methods for communicating between different "nodes".
The protocol builds on top of HTTP POST requests - usually via [ProtoPost](https://github.com/tehzevo/protopost) (and its [Python variant](https://github.com/tehzevo/protopost-python)).
Aegis nodes should also leverage Docker to avoid dependency issues and encourage portability.

Each node represents a different type of microservice such as [reinforcement learning agents](https://github.com/tehzevo/aegis-ppo),
[TensorBoard loggers](https://github.com/tehZevo/aegis-tensorboard),
and [Gaussian linear interpolation samplers](https://github.com/tehZevo/aegis-gaussian-lerp). As all nodes rely on POST requests, they can be easily linked together, even across hosts. This also makes building clients a breeze, as Aegis is compatible with anything that supports POST requests.

## Experiments
See [Aegis Experiments](https://github.com/tehZevo/aegis-experiments) for experiments.

## Nodes
* Utility/FP
  * [Distribute](https://github.com/tehZevo/aegis-distribute) - When called, forwards the provided data to multiple other nodes
  * [Pipe](https://github.com/tehZevo/aegis-pipe) - Call nodes in order, with data passed from one to the next. Operates sort-of like FP "pipe" functions.
* RL
  * [Vanilla Env](https://github.com/tehZevo/aegis-vanilla-env) - Run [Gym](https://github.com/openai/gym) environments as Aegis nodes
  * [PPO](https://github.com/tehZevo/aegis-ppo) - Run [Stable Baselines](https://github.com/hill-a/stable-baselines) PPO2 agents as Aegis nodes
* NN/compute
  * [ESN](https://github.com/tehZevo/aegis-esn) - Echo state networks with sparse input/output mapping support
  * [Projection](https://github.com/tehZevo/aegis-projection) - Projects one shape into another with a fully connected and optionally squashed neural network layer.
* Logging
  * [Tensorboard](https://github.com/tehZevo/aegis-tensorboard) - Log scalars and histograms via Aegis function calls
* Generators
  * [Gaussian Lerp](https://github.com/tehZevo/aegis-gaussian-lerp) - Generates interpolations between Gaussian samples

## TODO
* Upload/document more nodes
