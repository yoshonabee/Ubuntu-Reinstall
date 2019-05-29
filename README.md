# Reinstall Ubuntu 18.04

### Install zsh

``` bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get update
sudo apt-get install zsh
sudo apt-get install powerline fonts-powerline
git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
vim ~/.zshrc #zsh-theme ys
chsh -s /bin/zsh
source ~/.zshrc
cd .oh-my-zsh
upgrade_oh_my_zsh
```

### Install cuda environment

#### Install Nvidia driver

``` bash
sudo add-apt-repository ppa:graphics-drivers/ppa 
sudo apt-get update
ubuntu-drivers devices
sudo apt-get install nvidia-driver-415
sudo service gdm3 start
reboot

nvidia-smi
```



#### Install cuda

```bash
sudo dpkg -i cuda-repo-ubuntu1804_10.0.130-1_amd64.deb
sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
sudo apt-get update
sudo apt-get install cuda

nvcc --version
```

#### Install cudnn

* <https://blog.csdn.net/huang826336127/article/details/86670925>

### Install python packages

``` bash
sudo apt-get update
sudo apt-get install python-pip python-dev
sudo -H pip install --upgrade pip

sudo -H pip3 install numpy \
pandas \
matplotlib \
opencv-python \
gensim \
html5lib \
ipython \
jupyter \
scipy \
scikit-learn

sudo -H pip3 install https://download.pytorch.org/whl/cu100/torch-1.1.0-cp36-cp36m-linux_x86_64.whl
sudo -H pip3 install torchvision torchtext

```

### Other Installations

#### Install Sublime Text 3

``` bash
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo apt-get install apt-transport-https
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
sudo apt-get update
sudo apt-get install sublime-text
```



#### Install Chrome

``` bash
Just Install through firefox, quite easy!
```

### File Process

* Projects and files in old ubuntu to new ubuntu
* Format the unused disk   **BE CAREFUL**
