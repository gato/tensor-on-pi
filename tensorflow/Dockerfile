FROM ubuntu:latest
RUN apt-get update && apt-get -y upgrade
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get install -y python3 python3-pip libatlas-base-dev wget gfortran libhdf5-dev libc-ares-dev libeigen3-dev libopenblas-dev libblas-dev liblapack-dev
RUN pip3 install --upgrade pip
RUN pip3 install --upgrade setuptools
RUN pip3 install pybind11
RUN pip3 install Cython==0.29.21
RUN pip3 install h5py
WORKDIR /tf
COPY tensorflow-2.3.0-cp38-cp38-linux_aarch64.whl .
RUN pip3 install -v -v -v tensorflow-2.3.0-cp38-cp38-linux_aarch64.whl
