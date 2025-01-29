# SSH Setup

1. You have the .pem file with you
2. Save it in a secure folder
bash
```
cd ~
nano my-key.pem
```
Then paste your .pem file key there and save it - `Ctrl+X` + `Y` + Press `Enter`
Then run this 
bash 
```
chmod 400 my-key.pem
```

4. Through terminal reach that folder where pem file is located and copy this path
5. When you want to connect your VS code or Cursor to this SSH - Press - `Ctrl/Cmd + Shit + P`
   Then copy this there with (updated path to .pem file) press `Enter`
bash
```
ssh -i /path/to/my-key.pem ubuntu@3.135.213.201
```
Then it will ask which file to update with new permissions for ssh
![image](https://github.com/user-attachments/assets/7cdbbc91-7808-4821-aa93-5b0079409d5b)
Go with `/Users/guneeshvats/.ssh/config`
and paste this there and save
bash
```
Host my-aws-server
    HostName 3.135.213.201
    User ubuntu
    IdentityFile ~/path/to/my-key.pem
```
Then you can open in your IDE using the command - 
bash
```
ssh my-aws-server

```
## Before installing anything run these commands
bash 
```
sudo apt update && sudo app upgrade -y
```

## Install Miniconda 
Run this 
bash
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh && bash Miniconda3-latest-Linux-x86_64.sh
```

## Install Docker and Docker-Compose
bash
```
sudo apt install -y docker.io && sudo systemctl enable --now docker
sudo usermod -aG docker $USER
sudo systemctl enable --now docker
docker --version
docker run hello-world
```
For Docker-Compose Now
bash
```
sudo apt install -y docker-compose
docker-compose --version
```

### Debugging if the Hello-World Command doesn't run 
If your username is something other than ubuntu, replace it accordingly:
bash
```
sudo usermod -aG docker ubuntu
sudo usermod -aG docker $USER
groups
```
after gorups you should see docker there 
bash
```
sudo systemctl restart docker
docker run hello-world
```


