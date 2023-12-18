FROM mcr.microsoft.com/azureml/openmpi4.1.0-ubuntu20.04

USER root:root

# Download new package version list
RUN apt-get update

# Install NFS stack

RUN apt-get install -y nfs-common fio

# Install Python dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt && rm requirements.txt

CMD ["bash"]
