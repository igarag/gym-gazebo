# Installation


#### Execution examples
##### Run example for qlearn:
terminal 1
```
cd gym-gazebo/gym_gazebo/envs/installation/
bash turtlebot_setup.bash
```
terminal 2
```
cd gym-gazebo/examples/turtlebot
python circuit_turtlebot_lidar_qlearn.py
```

##### Run example for dqn:
terminal 1
```
cd gym-gazebo/gym_gazebo/envs/installation/
bash turtlebot_nn_setup.bash
```
terminal 2
```
cd gym-gazebo/examples/turtlebot
python circuit_turtlebot_lidar_qlearn.py
```


##### Using Neural Networks
This part of the installation is required only for the environments using DeepQLearning.

###### Keras and Theano installation
```bash
# install dependencies

sudo apt-get install gfortran

# install sript specific dependencies (temporal)
sudo apt-get install python-skimage

# install Theano
git clone git://github.com/Theano/Theano.git
cd Theano/
sudo python setup.py develop

#isntall Keras
sudo pip install keras
```
dot_parser error fix:
```bash
sudo pip install --upgrade pydot
sudo pip install --upgrade pyparsing
```
###### Enablig GPU for Theano

Follow the instructions [here](http://deeplearning.net/software/theano/install.html#gpu-linux) and change $PATH instead of $CUDA_ROOT.

Working on a clean installation of Ubuntu 18.04 using CUDA 10.0.

The following flags are needed in order to execute in GPU mode, using an alias is recommended.
```bash
THEANO_FLAGS=mode=FAST_RUN,device=gpu,floatX=float32
```

---

#### Gazebo gym

```bash
cd 
git clone https://github.com/erlerobot/gym-gazebo
cd gym-gazebo
sudo pip3 install -e .
```

If successful, expect something like [this](https://gist.github.com/vmayoral/4a1e5999811ac8bfbf7875670c430d27).


