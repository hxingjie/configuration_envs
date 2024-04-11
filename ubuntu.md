# Record

## route
make boot

sudo apt-get update
sudo apt-get install tar
sudo apt-get install vim

solve wireless
1. download https://www.intel.cn/content/www/cn/zh/support/articles/000005511/wireless.html
2. tar iwlwifi-ty-59.601f3a66.0.tgz
3. cp iwlwifi-ty-a0-gf-a0-59.ucode /lib/firmware

sudo apt install g++
sudo apt install make
sudo apt install gdb

sudo apt install git

pip library_name --update

install git lfs
tar -xvf *.gz
bash install.sh

ubuntu-drivers devices  # nvidia driver
sudo apt install nvidia-driver-550
shutdown -r now
nvidia-smi

conda install -c nvidia cuda-compiler  # cuda-compiler
nvcc -- version


## linux commands
apt update
apt install sudo
sudo su
adduser hxj # add user
su hxj # change to normal user
root: chmod 777 /etc/sudoers
vi sudoers
hxj ALL=(ALL:ALL) ALL

tar: tar -xvf *.tgz

shutdown -h now
shutdown -r now

ifconfig

sudo apt install ./*.deb

vim *
mkdir *
mv * path
rm filename
rm -r dirname

sudo adduser username


## conda command
install Anaconda3-2024.02-1-Linux-x86_64.sh
sudo bash Anaconda.sh
set pash: /home/anaconda3
let normal user can use: hxj@ubuntu-hxj:~$ /home/anaconda3/bin/conda init bash

conda --version
conda info
conda create --name envsname
conda activate envsname

conda install anaconda-clean
anaconda clean
rm -rf ./anaconda3/
rm -rf ~/.condarc ~/.conda ~/.continuum
vim ~/.bashrc  # del conda
source ~/.bashrc

conda install pytorch==2.2.0 pytorch-cuda=12.1 -c pytorch -c nvidia

import torch
import torchtext

print(torch.__version__)  # 2.1.2
print(torch.version.cuda)  # 11.8
print(torch.backends.cudnn.version())  # 8700

torch.cuda.is_available()
torch.cuda.device_count()
torch.cuda.device.get_device_name(0)

gpu = torch.device('cuda')
x = torch.rand(5,3).to(gpu)
x: tensor([[3.3000e-01, 7.9273e-01, 4.6684e-01],
        [6.6042e-04, 9.2719e-01, 9.1276e-01],
        [5.9449e-01, 1.7616e-01, 7.3718e-01],
        [8.4496e-01, 9.6554e-01, 8.8205e-01],
        [9.8886e-01, 2.7237e-01, 8.9327e-01]], device='cuda:0')

