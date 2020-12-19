# Aegis Project

## What is it?
The Aegis Project (or just "Aegis") is an exploration of combining concepts such as reinforcement learning, transfer learning, microservices, and automation.
At its core, it provides standard methods for communicating between different "nodes".
The protocol builds on top of HTTP POST requests - usually via [ProtoPost](https://github.com/tehzevo/protopost) (and its [Python variant](https://github.com/tehzevo/protopost-python))

Each node represents a different type of microservice such as [reinforcement learning agents](https://github.com/tehzevo/aegis-ppo),
[TensorBoard loggers](https://github.com/tehZevo/aegis-tensorboard),
and [Gaussian linear interpolation samplers](https://github.com/tehZevo/aegis-gaussian-lerp). As all nodes rely on POST requests, they can be easily linked together, even across hosts. This also makes building clients a breeze, as Aegis is compatible with anything that supports POST requests.

## TODO
* List of Aegis nodes
