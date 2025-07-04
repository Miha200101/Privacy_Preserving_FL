# PrivacyFL - Federated Learning Simulator

This repository contains a basic simulator for federated learning. The setup includes multiple clients and a central server that work together to train a model using distributed data.

The goal is to show how federated learning works in practice, with or without differential privacy.

## 📦 What this project does

- Simulates training with 3 clients and 1 server
- Uses logistic regression on MNIST data (by default)
- Can enable/disable privacy and security settings
- Logs metrics such as accuracy and training time

## 🚀 How to run it

1. Clone the repository:

`git clone https://github.com/Miha200101/Privacy_Preserving_FL.git`
`cd Privacy_Preserving_FL`


2. Create and activate the environment:

`conda env create -f environment.yml -n Privacy_Preserving_FL`
`conda activate Privacy_Preserving_FL`


1. Run the simulation:

`cd src`
`python run_simulation.py`

## ⚙️ Configuration

All important settings can be adjusted in `src/config.py`:

 `USE_DP_PRIVACY`: enable/disable differential privacy
 `USE_SECURITY`: enable/disable secure communication
 `USING_CUMULATIVE`: control if data grows at each iteration
 `NUM_CLIENTS`, `NUM_SERVERS`, `ITERATIONS`: simulation scale

## 📁 Structure

 `src/client_agent.py`: logic for clients
 `src/server_agent.py`: logic for the server
 `src/initializer.py`: sets up and runs the simulation
 `src/config.py`: global settings

## 📊 Output Example

Performance Metrics for client_agent0
Personal accuracy: 0.82
Federated accuracy: 0.85
Training time: 1.2s
