#!/bin/bash

sudo apt update -y
sudo apt install docker.io -y
sudo systemctl enable docker

sudo swapoff -a
sudo sed -i '/swap/d' /etc/fstab

sudo apt install apt-transport-https curl -y
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

cat <<EOF | sudo tee /etc/apt/sources.list.d/kubernetes.list
deb https://apt.kubernetes.io/ kubernetes-xenial main
EOF

sudo apt update
sudo apt install kubelet kubeadm kubectl -y
