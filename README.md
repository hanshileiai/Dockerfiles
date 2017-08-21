## docker install 
### ubuntu 15.10 (docker 1.12)
```
sudo apt-get remove docker docker-engine
sudo curl -s 'https://sks-keyservers.net/pks/lookup?op=get&search=0xee6d536cf7dc86e2d7d56f59a178ac6c6238f52e' | sudo apt-key add --import
sudo apt-get update && sudo apt-get install apt-transport-https
sudo apt-get install -y linux-image-extra-virtual
```
```
echo "deb https://packages.docker.com/1.12/apt/repo ubuntu-wily main" | sudo tee /etc/apt/sources.list.d/docker.list
sudo apt-get update
sudo apt-get upgrade docker-engine
sudo docker -v
```
### ubuntu 14.04,16.04 (docker 17)
```
sudo apt-get remove docker docker-engine docker-ce
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```
```
sudo apt-get update
sudo apt-cache policy docker-ce
sudo apt-get install -y docker-ce
sudo docker -v
```

## docker-compose install 
```
sudo curl -o /usr/local/bin/docker-compose -L "https://github.com/docker/compose/releases/download/1.15.0/docker-compose-$(uname -s)-$(uname -m)"
sudo chmod +x /usr/local/bin/docker-compose
sudo docker-compose -v
```