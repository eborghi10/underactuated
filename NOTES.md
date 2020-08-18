# My personal notes of Underactuated Robotics

# Introduction

Taking notes in the [internal online textbook](http://underactuated.mit.edu/).

# Running notebooks locally

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

# 1: Fully-actuated vs Underactuated Systems

- [Notes](http://underactuated.mit.edu/intro.html)
- [Class](https://www.youtube.com/watch?v=VeEqtTgDXFc&t=3569s)
- Notebooks
	- [Dynamics of the double pendulum](https://github.com/RussTedrake/underactuated/blob/master/examples/double_pendulum/dynamics.ipynb)
	- [Feedback Cancellation of the Double Pendulum](https://github.com/RussTedrake/underactuated/blob/master/examples/double_pendulum/feedback_cancellation.ipynb)
