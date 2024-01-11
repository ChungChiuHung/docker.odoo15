# odoo dev
Create an Odoo development environment using Docker via WSL (Windows Subsystem for Linux) in VSCode.

# Install Docker Compose
To install Docker Compose on Ubuntu, you can follow these steps:
1. Update the package lists for upgrades and installations:
```sh
sudo apt update
```
2. Install Docker Compose using the curl command:
```sh
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
3. Apply executable permissions to the Docker Compose binary:
```sh
sudo chmod +x /usr/local/bin/docker-compose
```
4. Verify the installation by checking the version of Docker Compose:
```sh
docker-compose --version
```
# Install Docker/Vscode Server on WSL Ubuntu
1. Update the package lists:
```sh
sudo apt update
```
2. Install Docker dependencies:
```sh
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
3. Add the Docker repository's GPG key:
```sh
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
4. Add the Docker repository:
    For x86_64/amd64 architecture:
```sh
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
5. Update the package lists again:
```sh
sudo apt update
```
6. Install Docker:
```sh
sudo apt install docker-ce docker-ce-cli containerd.io
```
7. Add your user to the 'docker' group:
```sh
sudo usermod -aG docker $USER
```
8. Restart & Verify Docker installation by running the Docker version command:
```sh
docker version
```
9. Create a folder
```sh
mkdir odoo_dev
```
10. Change the ownership of a directory and its child folders/files
```sh
sudo chown -R $USER:$USER /folder/to/path
```
 - get the current folder path
 ```sh
 pwd
 ```
11. Install Vscode Server
```sh
code .
```
# Vscode
1. Create a docker-compose.yml file
2. Start the server and database using Docker Compose
```sh
sudo docker-compose up -d
```
Store/Change the Odoo Master Password
xxxx-xxxx-xxxx

## Optional
### Get into a container name "Container_Name" and start in interactive Bash shell
```sh
docker exec -it Container_Name bash
docker exec -it --user root Container_Name /bin/bash
```
### Install Package in the Odoo Docker container
```sh
apt-get update
pip install pypeg2
pip install ecpay_invoice3
apt-get install ttf-wqy-zenhei ttf-wqy-microhei -y
```
### To clone a GitHub repository to a specific folder on your local machine using Git
```sh
git clone <repository_url> <folder_path>
```
example:
```sh
git clone https://github.com/username/example-repo ~/Desktop/my-project
```
