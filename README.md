# odoo
Create an Odoo development environment using Docker via WSL (Windows Subsystem for Linux) in VSCode.
# Install Docker on WSL Ubuntu
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
8. Verify Docker installation by running the Docker version command:
```sh
docker version
```
9. Create a folder
```sh
mkdir odoo_dev
```
10. 


## Store/Change the Odoo Master Password
xxxx-xxxx-xxxx

# Get into a container name "Container_Name" and start in interactive Bash shell
```sh
docker exec -it Container_Name bash
docker exec -it --user root Container_Name /bin/bash
```
# Install Package in the Odoo Docker container
```sh
apt-get update
pip install pypeg2
pip install ecpay_invoice3
apt-get install ttf-wqy-zenhei ttf-wqy-microhei -y
```
