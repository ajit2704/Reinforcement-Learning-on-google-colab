# Reinforcement Learning on google colab

# Colab notebook links

1. [gym_intro](https://colab.research.google.com/drive/1AsFzJDEI9OtlmGHyuqr21iMLKy4OgAMg)
2. [crossentropy_method](https://colab.research.google.com/drive/1Nu7NtjIQG2MRB2TnQ63RW4E9n_2MNblR)
3. [qlearning](https://colab.research.google.com/drive/1nDO-XfgkAgABCe2jYNAFwmi4plr2xJoc)
4. [Actor-Critic](https://colab.research.google.com/drive/1-TiI1dNIQDukkQC1PXy7mhDT883j9ua9)

# Guide to follow
Google Colaboratory provides that 12GB GPU support with continuous 12 hr runtime. For RL it requires to render the environment visuals. Here is sort of a tutorial to get over that issue & continue free coding.

Motive of this blog will be to use gym & gym[atari] on colab. For Deep Learning & other setup you may want to refer this article, it will also give you the basic understanding.

Most of the requirements of python packages are already fulfilled on colab. To run gym, 1st you have to install prerequisites like xvbf,opengl & other python-dev packages:

```
!apt-get install -y python-numpy python-dev cmake zlib1g-dev libjpeg- dev xvfb libav-tools xorg-dev python-opengl libboost-all-dev libsdl2-dev swig
```

![](https://github.com/ajit2704/Practical-Reinforcement-Learning-With-Colab/blob/master/1_yqDjbLhneoEAyL8Lbwj43w.png)

Now for rendering environment I prefer to use pyvirtualdisplay, so to fulfill that:

```
   !pip install pyvirtualdisplay
   !pip install piglet
```

![](https://github.com/ajit2704/Practical-Reinforcement-Learning-With-Colab/blob/master/1_s4eFRgsGnHWmJWzgAe52Lg.png)

To activate virtual display we need to run a script once for training an agent, as follows:

```python
from pyvirtualdisplay import Display
display = Display(visible=0, size=(1400, 900))
display.start()
```

Moving on to gym requirements, gym is already installed but not with atari game environments, to get that:

```
!pip install gym
!pip install “gym[atari]"
```

# References
 1. For gym, check the https://gym.openai.com/docs/
 2. For colab, checkout https://medium.com/deep-learning-turkey/google-colab-free-gpu-tutorial-e113627b9f5d
