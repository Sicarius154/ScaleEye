# ScaleEye
An experimental auto-scaler for Kubernetes written in Scala. Written as a part of an undergraduate dissertation.

# Setup and Organisation
This repository acts as the glue between two distinct projects, [Watcher](https://github.com/Sicarius154/Watcher) and [Scaling Engine](https://github.com/Sicarius154/ScalingEngine). These two components, when brought together create the Scale Eye autoscaler. The two repositories are included in this repository as Git submodules, but any changes or work on these two components should be completed in the proper repositories and pulled into this repository, as opposed to being added to this repositories' checkout.

# Design and Algorithms
All system design and algorithm design is discussed in detail in the paper included in this repository, it is recomended anyone that wishes to understand how this auto-scaler works reads that paper, particularly chapters 4 through to 6 inclusive. 

# Building and Running
The entire autoscaler should be deployed using Docker Compose. Please ensure you have the most up-to-date version of Docker installed, and then follow the steps below. Please not that these steps outline how to deploy the autoscaler, deploying an app to scale is out of scope for these instructions but deploying a mock application such as [Google Cloud Online Boutique Demo](https://github.com/GoogleCloudPlatform/microservices-demo) is recomended alongside the [Istio Service Mesh](https://istio.io). 

Deplpoyment is made very simple thanks to the usage of Docker compose which will deoloy both components as well as the Kafka instance needed in order to have the two components communicate. 

1. Clone this repository
2. CD into this repository's root 
3. type `docker-compose up -d`
4. Wait for the autoscaler to start
5. Done

