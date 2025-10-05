# PPO_RL

**Implementation of the Proximal Policy Optimization (PPO) algorithm using TensorFlow for reinforcement learning tasks.**

This repository provides a clean and reproducible implementation of PPO, a popular on‑policy reinforcement learning algorithm that balances ease of tuning with strong empirical performance. It includes a training notebook, scripts for continuous control tasks, and explanations of the core concepts behind PPO and its clipped surrogate loss.

## Features

- **TensorFlow implementation:** Uses TensorFlow 2.x with eager execution for clarity and performance.
- **Environment support:** Configured for OpenAI Gym continuous control environments such as *CartPole*, *Pendulum*, and *MountainCar*. Easily extendable to other Gym environments.
- **Clipped surrogate objective:** Implements PPO’s clipping mechanism to prevent large policy updates and stabilize learning.
- **Advantage estimation:** Supports both generalized advantage estimation (GAE) and standard advantage computation.
- **Training notebook & script:** Jupyter notebook for interactive experimentation and a Python script for reproducible training runs.
- **Logging & plotting:** Tracks rewards, losses and other metrics during training and produces plots for easy analysis.

## Repository Structure

- `ppo.py` – Core implementation of the PPO agent and training loop.
- `train.py` – Example script to train a PPO agent on a specified Gym environment.
- `notebooks/PPO_training.ipynb` – Interactive notebook demonstrating training on CartPole and other tasks.
- `requirements.txt` – List of Python dependencies.
- `utils/` – Helper functions for logging, plotting and environment wrappers.

## Getting Started

1. **Clone the repository**:

   ```bash
   git clone https://github.com/IamArmanNikkhah/PPO_RL.git
   cd PPO_RL
   ```

2. **Install dependencies** (preferably in a virtual environment):

   ```bash
   pip install -r requirements.txt
   ```

   The key dependencies include:
   - `tensorflow>=2.4`
   - `gym>=0.21`
   - `numpy`, `matplotlib`, and `tqdm`

3. **Run the training script**:

   ```bash
   python train.py --env Pendulum-v1 --timesteps 50000
   ```

   You can change `--env` to any Gym environment with a continuous action space. Use `--help` to see all configuration options.

4. **Use the notebook**: Launch the Jupyter notebook to step through the training process interactively:

   ```bash
   jupyter notebook notebooks/PPO_training.ipynb
   ```

## Usage & Customization

- **Configuring hyperparameters:** Modify the `config` dictionary in `train.py` or pass command-line arguments to change learning rate, clip ratio, number of epochs, batch size and more.
- **Adding environments:** To train on new environments, ensure they follow the OpenAI Gym API and adjust observation/action dimensions accordingly.
- **Monitoring training:** The script logs episode rewards and losses to the console and saves them to a file. Use the provided plotting utilities to visualize learning curves.

## Contributing

Contributions and improvements are welcome! If you find bugs, want to add new features (e.g., support for discrete action spaces or PyTorch implementation), or improve documentation, please open an issue or submit a pull request.

1. Fork the repository and create your branch:

   ```bash
   git checkout -b feature/YourFeature
   ```

2. Commit your changes:

   ```bash
   git commit -m "Add YourFeature"
   ```

3. Push to the branch and open a pull request.

## License

This project is licensed under the MIT License – feel free to use it for research or educational purposes.
