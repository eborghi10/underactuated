# My personal notes of [Underactuated Robotics](https://courses.edx.org/courses/course-v1:MITx+6.832x_2+3T2015/courseware)

## Introduction

Taking notes in the [internal online textbook](http://underactuated.mit.edu/).

## Running notebooks locally

- Clone the underactuated repository and build the image:

```sh
git clone git@github.com:eborghi10/underactuated.git

cd underactuated

docker build -f scripts/docker/Dockerfile -t robotlocomotion/underactuated:latest .
```

- Run docker image (being inside `underactuated`) and export underactuated `PYTHONPATH`:

```sh
docker run -i -p 7000:7000 -p 8888:8888 -t -v $(pwd):/root/underactuated -w /root/underactuated robotlocomotion/underactuated:latest

export PYTHONPATH=`pwd`:${PYTHONPATH}
```

- Execute the Jupyter notebooks and click on the link that it'll generate:

```sh
$ jupyter notebook --ip=0.0.0.0 --port=7000 --allow-root

http://0.0.0.0:7000/?token=<TOKEN_GOES_HERE>
```

## Class notes

### 1: Fully-actuated vs Underactuated Systems

- [Notes](http://underactuated.mit.edu/intro.html)
- [Class](https://www.youtube.com/watch?v=VeEqtTgDXFc)
- Notebooks
  - [Dynamics of the double pendulum](https://github.com/RussTedrake/underactuated/blob/master/examples/double_pendulum/dynamics.ipynb)
  - [Feedback Cancellation of the Double Pendulum](https://github.com/RussTedrake/underactuated/blob/master/examples/double_pendulum/feedback_cancellation.ipynb)

### 2: The Simple Pendulum

- [Notes](http://underactuated.mit.edu/pend.html)
- [Class](https://www.youtube.com/watch?v=LjIcxrxeW44)
- Notebooks
  - [Simple Pendulum in Python](https://github.com/RussTedrake/underactuated/blob/master/examples/pendulum/torque_slider_demo.ipynb)
  - [Nonlinear autapse](https://github.com/RussTedrake/underactuated/blob/master/examples/autapse_and_lstm.ipynb)
  - [Energy Shaping for the Pendulum](https://github.com/RussTedrake/underactuated/blob/master/examples/pendulum/energy_shaping.ipynb)
- Exercises
  - [Attractivity vs Stability](https://github.com/RussTedrake/underactuated/blob/master/exercises/pend/attractivity_vs_stability/attractivity_vs_stability.ipynb)
  - [Pendulum with Vibrating Base](https://github.com/RussTedrake/underactuated/blob/master/exercises/pend/vibrating_pendulum/vibrating_pendulum.ipynb)

### 7: Dynamic Programming

- [Notes](http://underactuated.mit.edu/dp.html)
- [Class](https://www.youtube.com/watch?v=GPvw92IKO44)
- ...

### 8: Linear Quadratic Regulators

- [Notes](http://underactuated.mit.edu/lqr.html)
- [Class](https://www.youtube.com/watch?v=UZpLHlDV4gA)
- ...

### 3: Acrobots, Cart-Poles, and Quadrotors

- [Notes](http://underactuated.mit.edu/acrobot.html)
- [Class]()
- Notebooks
   - []()
