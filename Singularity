Bootstrap: docker
From: ubuntu:18.04

%environment
PATH=/usr/local/src/FastQC:$PATH
export LC_ALL=C

%post
apt-get update 
apt-get dist-upgrade -y 
apt-get install wget build-essential unzip openjdk-11-jre -y 
rm -rf /var/lib/apt/lists/*
mkdir -p /usr/local/src
cd /usr/local/src && \
wget http://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.7.zip -O fastqc.zip && \
unzip fastqc.zip && \
rm fastqc.zip && \
chmod +X FastQC/fastqc && \
chmod 755 FastQC/fastqc

%labels
MAINTAINER BioBox
Version v1.0
