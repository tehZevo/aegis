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

- RL
  - Environments
    - [Vanilla Env](https://github.com/tehZevo/aegis-vanilla-env) - Run [Gym](https://github.com/openai/gym) environments as Aegis nodes
    - [Mario](https://github.com/tehZevo/aegis-mario) - Super Mario Bros. environments thanks to [gym-super-mario-bros](https://github.com/Kautenja/gym-super-mario-bros)
  - Agents
    - [PPO](https://github.com/tehZevo/aegis-ppo) - Run [Stable Baselines](https://github.com/hill-a/stable-baselines) PPO2 agents as Aegis nodes

- Vision (CV)
  - [Keras Application](https://github.com/tehZevo/aegis-keras-app) - Run inference on pretrained [Keras Applications](https://keras.io/api/applications/) as Aegis nodes
  - [Image Stylization](https://github.com/tehZevo/aegis-image-stylizer) - Stylize images thanks to [arbitrary-image-stylization-tfjs](https://github.com/reiinakano/arbitrary-image-stylization-tfjs)
  - [Face Detector](https://github.com/tehZevo/aegis-face-detector) - Detect faces
  - [Age/Gender Predictor](https://github.com/tehZevo/aegis-age-gender-predictor) - Predict age and gender of faces
  - [YOLO](https://github.com/tehZevo/aegis-yolo) - Object detection inference

- Language (NLP)
  - [TTS](https://github.com/tehZevo/aegis-tts) - Text to Speech using [Coqui TTS](https://github.com/coqui-ai/TTS)
  - [Textgen](https://github.com/tehZevo/aegis-textgen) - Text generation powered by [aitextgen](https://github.com/minimaxir/aitextgen)

- Other NN/compute
  - [ESN](https://github.com/tehZevo/aegis-esn) - Echo state networks with sparse input/output mapping support
  - [Projection](https://github.com/tehZevo/aegis-projection) - Projects one shape into another with a fully connected and optionally squashed neural network layer
  - [Autoencoder](https://github.com/tehZevo/aegis-ae) - Autoencoders with support for encoding/decoding inputs/latents as well as calculating reconstruction losses for inputs

- Logging & visualization
  - [Tensorboard](https://github.com/tehZevo/aegis-tensorboard) - Log scalars and histograms via Aegis function calls
  - [Visualizer](https://github.com/tehZevo/aegis-visualizer) - View ND-arrays and base64-encoded images in your browser

- Generators
  - [Gaussian Lerp](https://github.com/tehZevo/aegis-gaussian-lerp) - Generates interpolations between Gaussian samples

- Utilities/FP
  - [Distribute](https://github.com/tehZevo/aegis-distribute) - When called, forwards the provided data to multiple other nodes
  - [Pipe](https://github.com/tehZevo/aegis-pipe) - Call nodes in order, with data passed from one to the next. Operates sort-of like FP "pipe" functions
  - [Web Crawler](https://github.com/tehZevo/aegis-crawler) - Recursively visit links and return page texts
  - [Image Annotator](https://github.com/tehZevo/aegis-image-annotator) - Draw boxes and labels on images
  - [Image Slicer](https://github.com/tehZevo/aegis-image-slicer) - Split a single image into multiple using bounding boxes
  - [Discord](https://github.com/tehZevo/aegis-discord) - Listen for and send messages on Discord
  - [Mailer](https://github.com/tehZevo/aegis-mailer) - Send emails via Aegis function calls
  - [Sheets](https://github.com/tehZevo/aegis-sheets) - Read from Google Sheets

## Non-node Utilities
- [ProtoPost](https://github.com/tehZevo/protopost) ([Python variant](https://github.com/tehZevo/protopost-python))
- [Keras model builder](https://github.com/tehZevo/keras-model-builder)
- [nd-to-json](https://github.com/tehZevo/nd-to-json)
- [img-to-b64](https://github.com/tehZevo/img-to-b64)
