# Elasticsearch-Kibana-Docker-compose


lsb_release -dirc

git clone https://github.com/mahesh1104/elk

sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
	
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
   
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io

docker --version

git clone https://github.com/mahesh1104/elk


sudo sysctl -w vm.max_map_count=262144

vi /etc/sysctl.d/anyname    (to make it permament) 
vi /etc/sysctl.conf/anyname (")

curl -L "https://github.com/docker/compose/releases/download/1.13.0/docker-compose-$(uname -s)-$(uname -m)" > ./docker-compose
sudo mv ./docker-compose /usr/bin/docker-compose
sudo chmod +x /usr/bin/docker-compose



base=https://github.com/docker/machine/releases/download/v0.16.0 &&
  curl -L $base/docker-machine-$(uname -s)-$(uname -m) >/tmp/docker-machine &&
  sudo install /tmp/docker-machine /usr/local/bin/docker-machine
  
 docker-machine version
 
sudo docker-compose up -d
 
 docker-compose ps
docker-compose logs -f
sudo netstat -nltp

 sg- tcp -5601 => we need to mention
 
 configure filebeat and enable system module 
 all the system logs to elastic search server.
 
  Kibana
  Elasticsearch output
  
  Run Elasticsearch & Kibana as docker containers
    git clone https://github.com/justmeandopensource/elk
    cd elk/docker
    mv docker-compose-v7.1.1.yml docker-compose.yml
    sudo sysctl -w vm.max_map_count=262144
    docker-compose up -d
	
Install Filebeat on client machine (Ubuntu 18.04)
    wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
    sudo apt-get install apt-transport-https
    echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
    sudo apt-get update && sudo apt-get install filebeat
	
Configure Filebeat and enable system module
    sudo vi /etc/filebeat/filebeat.yml
	
	sudo filebeat modules enable system
    sudo filebeat test config
    sudo filebeat test output
    sudo filebeat setup
    sudo systemctl start filebeat
	
	
Install and setup elastalert




sudo logger -t MAHESH hello this is test
	
	vi /etc/postfix/main.cf
	vi /etc/postfix/sasl_passwd
	
	
   	
