---
{"dg-publish":true,"permalink":"/reinforcement-learning/","created":"","updated":""}
---


#resources #RL

# Reinforcement Learning

If you have heard of RL, you have inevitably heard of the wonderful [Sutton Barto book](http://incompleteideas.net/book/RLbook2020.pdf), which is an excellent resource to get started with. However, if you're anything I am and get easily bored with books, there is a vast amount of incredibly useful resources that may help you absorb the material much quicker and in much more depth. Here are some that I have found useful:

## Lecture series

If you're new to RL, the first ones I would recommend would be:

- [David Silver's RL course](https://youtube.com/playlist?list=PLzuuYNsE1EZAXYR4FJ75jcJseBmo4KQ9-), and
- [Martha & Adam White's RL specialization](https://www.coursera.org/specializations/reinforcement-learning#courses) if you can spare a little more time

Once you have a decent grasp of the basics, I would highly recommend the following courses from the Berkeley and Stanford giants that will surely take you to the state-of-the-art RL:

- [Pieter Abbeel's Foundations of Deep RL](https://youtube.com/playlist?list=PLwRJQ4m4UJjNymuBM9RdmB3Z9N5-0IlY0)
- [Sergey Levine's Berkeley CS285 course](https://youtube.com/playlist?list=PL_iWQOsE6TfURIIhCrlt-wj9ByIVpbfGc)
- [Chelsea Finn's Stanford CS330 course](https://youtube.com/playlist?list=PLoROMvodv4rMIJ-TvblAIkw28Wxi27B36)
- [Deep RL Bootcamp 2017](https://www.youtube.com/playlist?list=PLXoDfcPNqdnkdhRCrCCdVUOtKOwuBhJdF)

## Blogs & wikis

- [RL discord wiki](https://github.com/andyljones/reinforcement-learning-discord-wiki/wiki) hosts a ton of useful resources with many overlaps. Newcomers may want to check out their [debugging advice](https://github.com/andyljones/reinforcement-learning-discord-wiki/wiki#debugging-advice) if nothing else
- [Lilian Weng's blog posts](https://lilianweng.github.io/archives/) are an invaluable resource and service to the community
- [OpenAI Spinning up](https://spinningup.openai.com/en/latest/) is a practically-oriented tutorial/course
- [BAIR blog](https://bair.berkeley.edu/blog/about/) has monthly RL highlights from Berkeley & around
- [RL weekly](https://v1.endtoend.ai/rl-weekly/ "https://v1.endtoend.ai/rl-weekly/") is a series of weekly (not anymore) RL highlights
- [Julien Vitay's blog](https://julien-vitay.net/deeprl/)
- [Jonathan Hui's Deep RL Series on Medium](https://jonathan-hui.medium.com/rl-deep-reinforcement-learning-series-833319a95530)

## Libraries

#### RL

- [Stable Baselines 3](https://github.com/DLR-RM/stable-baselines3) is one that I have extensively used and prefer
- [RLlib](https://docs.ray.io/en/latest/rllib/index.html) is a library for large-scale distributed RL applications
- [Clean RL](https://github.com/vwxyzjn/cleanrl) is one I haven't used but heard great things about
- [My SB3 vs RLlib github repository](https://github.com/nisheetpatel/sb3-vs-rllib) benchmarking their performance and some of [my notes on working with SB3 & RLlib](https://github.com/nisheetpatel/sb3-vs-rllib/blob/main/docs/notes_sb3_vs_rllib.md)

##### Imitation Learning

- [Imitation](https://github.com/HumanCompatibleAI/imitation) has several SOTA imitation learning algorithms
- [Seals](https://github.com/HumanCompatibleAI/seals) is the sister library for imitation with all environments

#### Environments

- [OpenAI gym environments](https://www.gymlibrary.dev/)
- [PyBullet Gym](https://github.com/benelot/pybullet-gym) open-source version of Mujoco
- [MuJoCo](https://github.com/deepmind/mujoco) the now-open-sourced physics engine for all control environments
- [MiniGrid](https://github.com/maximecb/gym-minigrid) minimalistic grid-world environments
- [MyoSuite](https://github.com/facebookresearch/myosuite) has a suite of tasks for musculoskeletal control
- [Unity ML-Agents](https://github.com/Unity-Technologies/ml-agents) enables games to serve as environments
- [ViZDoom](https://github.com/mwydmuch/ViZDoom) for Reinforcement Learning from Raw Visual Information
- [Deepmind Control suite](https://github.com/deepmind/dm_control)
- [OpenSpiel](https://github.com/deepmind/open_spiel) RL search and planning games
- [Meta-World](https://meta-world.github.io/) for multi-task meta RL
- [CARLA](http://carla.org/) open-source simulator for self-driving cars
- [PettingZoo](https://www.pettingzoo.ml/) multi-agent RL environments
- [Awesome RL environment list](https://github.com/clvrai/awesome-rl-envs)