FROM pytorch/pytorch:2.1.2-cuda12.1-cudnn8-devel

RUN apt update
RUN apt install -y git

WORKDIR /workspace
RUN git clone https://github.com/oobabooga/text-generation-webui.git -b snapshot-2024-04-28
WORKDIR /workspace/text-generation-webui
RUN pip install -r requirements.txt
RUN pip uninstall -y flash-attn
