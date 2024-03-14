# Cube Stacking RL

This project aims to develop a reinforcement learning (RL) agent that can stack cubes in a simulated environment.

## Prerequisites

Before getting started, make sure you have the following installed:

- Python 3.x
- RL libraries (e.g., OpenAI Gym, Stable Baselines3)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/cube_stacking_rl.git
    ```

2. Navigate to the project directory:

    ```bash
    cd cube_stacking_rl
    ```

3. Create a virtual environment (optional but recommended):

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

4. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. download the dataset
    '''bash
    python -m mani_skill2.utils.download_demo "StackCube-v0"
    '''
2. Convert the dataset into trajectories:

    ```bash
    python -m mani_skill2.trajectory.replay_trajectory --traj-path demos/rigid_body/LiftCube-v0/trajectory.h5 --save-traj -o state -c pd_ee_delta_pose --num-procs 8
    ```

3. Train the agent:

    ```bash
    python state_imitation_learning_stackcube.py --demos=demos/v0/rigid_body/StackCube-v0/trajectory.state.pd_ee_delta_pose.h5
    ```

    This will load the trained model and evaluate its performance.

## Contributing

If you would like to contribute to this project, follow these steps:

1. Fork the repository on GitHub.

2. Clone your forked repository:

    ```bash
    git clone https://github.com/your-username/cube_stacking_rl.git
    ```

3. Create a new branch for your changes:

    ```bash
    git checkout -b feature/your-feature-name
    ```

4. Make your changes and commit them:

    ```bash
    git commit -m "Add your commit message here"
    ```

5. Push your changes to your forked repository:

    ```bash
    git push origin feature/your-feature-name
    ```

6. Open a pull request on GitHub.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.