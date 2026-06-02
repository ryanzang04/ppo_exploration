# PPO Exploration Experiments

This repository contains custom PPO experiments based on CleanRL, with added exploration bonuses for studying curiosity-driven reinforcement learning.

## Files

- `ppo.py`: Standard PPO baseline.
- `ppo_rnd.py`: PPO with a Random Network Distillation (RND) exploration bonus.
- `ppo_icm.py`: PPO with an Intrinsic Curiosity Module (ICM) exploration bonus.

## Example Commands

Run PPO with RND:

```bash
python ppo_rnd.py --env-id CartPole-v1 --exploration rnd --rnd-coef 0.01 --total-timesteps 200000
```

Run PPO with ICM:

```bash
python ppo_icm.py --env-id CartPole-v1 --exploration icm --icm-coef 0.01 --total-timesteps 200000
```

Run the standard PPO baseline:

```bash
python ppo.py --env-id CartPole-v1 --total-timesteps 200000
```

## Plotting Results

Training logs are saved in the `runs/` directory. To view results with TensorBoard, run:

```bash
tensorboard --logdir runs
```

Then open the local TensorBoard URL shown in the terminal.
