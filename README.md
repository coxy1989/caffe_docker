# caffe_docker

This repository provides a recipe - in the from of instruction and Dockerfile for running GPU caffe workloads out of a docker container.

## Recipe

1. Configure nvidia docker: follow [these instructions](https://gist.github.com/Brainiarc7/a8ab5f89494d053003454efc3be2d2ef).
- Verify your nvidia docker configuration: `sudo docker run --runtime=nvidia --rm nvidia/cuda nvidia-smi`
- Build the docker image from the dockerfile included in this repo: `docker build -t caffe .`
- Run it: `run -it --runtime=nvidia --shm-size=8g --rm caffe`
- Verify all is well by running throuch [one of the caffe examples](http://caffe.berkeleyvision.org/gathered/examples/mnist.html).



