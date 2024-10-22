# Kafka Local Developer Setup
A guide to setting up a local Kafka development environment with minikube and a bunch of different cluster configurations.


## Getting started
1. `minikube delete && minikube start --memory 8576 --cpus 4`
2. `kubectl apply --kustomize ./environments/base/strimzi-base/0.43.0/crds && sleep 5 && kubectl apply --kustomize ./environments/base/strimzi-base/0.43.0/templates`
3. Deploying a specific environment: `export EXAMPLE=single-broker && kubectl apply --kustomize ./environments/$EXAMPLE/`