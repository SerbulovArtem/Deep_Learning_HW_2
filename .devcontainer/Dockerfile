FROM runpod/pytorch:1.0.2-cu1281-torch280-ubuntu2404

ENV NVIDIA_VISIBLE_DEVICES=all
ENV NVIDIA_DRIVER_CAPABILITIES=compute,utility

WORKDIR /workspaces/HW2

COPY requirements.txt /tmp/requirements.txt

RUN apt-get update \
	&& apt-get remove --purge -y python3-blinker python3-cryptography \
	&& pip install --no-cache-dir -r /tmp/requirements.txt