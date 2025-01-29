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
5. When you want to connect your VS code or Cursor to this SSH
bash
```
ssh -i /path/to/my-key.pem ubuntu@3.135.213.201
```
7. Install Miniconda using this command
