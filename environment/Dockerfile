# hash:sha256:af8f012856a9dcd4ef48915ac0173ae60d310c3ff7aafafb75ba009f353fb88c
FROM registry.codeocean.com/codeocean/miniconda3:4.9.2-cuda11.7.0-cudnn8-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive

RUN pip install -U --no-cache-dir \
    numpy==1.21.2 \
    pandas==1.3.2 \
    pillow==9.5.0 \
    scikit-learn==1.1.1 \
    scipy==1.7.1 \
    tensorboard==2.10.1 \
    tensorboard-data-server==0.6.1 \
    tensorboard-plugin-wit==1.8.1 \
    tensorboardx==2.5.1 \
    torchmetrics==0.10.3 \
    tqdm==4.62.2

ADD "https://github.com/coder/code-server/releases/download/v4.9.0/code-server-4.9.0-linux-amd64.tar.gz" /.code-server/code-server.tar.gz
	
RUN cd /.code-server \
	&& tar -xvf code-server.tar.gz \
	&& rm code-server.tar.gz \
	&& ln -s /.code-server/code-server-4.9.0-linux-amd64/bin/code-server  /usr/bin/code-server

COPY postInstall /
RUN /postInstall
