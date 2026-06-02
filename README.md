# PPO Exploration Experiments

This repository contains custom standard PPO experiments with exploration bonuses.

## Files

- `ppo_rnd.py`: PPO with Random Network Distillation exploration bonus.
- `ppo_icm.py`: PPO with Intrinsic Curiosity Module exploration bonus.

## Example commands
```bash
python ppo_rnd.py --env-id CartPole-v1 --exploration rnd --rnd-coef 0.01 --total-timesteps 200000
python ppo_icm.py --env-id CartPole-v1 --exploration icm --icm-coef 0.01 --total-timesteps 200000