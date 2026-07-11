 ### Devops Introduction
bash <(curl -sL https://tinyurl.com/3w6rac3n)

🚀 Database Installations
Setup MySQL on Ubuntu Instances

📌 MySQL Database on Ubuntu 24.04 Instance
# Update and Install MySQL
sudo apt update && sudo apt upgrade -y
sudo apt install mysql-server -y
sudo mysql --version

# Configure MySQL for Password and Remote Login
sudo mysql

# Inside the MySQL shell, run the following: Updated by SAK
CREATE USER IF NOT EXISTS 'root'@'%' IDENTIFIED BY '1234';
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' WITH GRANT OPTION;
FLUSH PRIVILEGES;
EXIT;

# Allow Remote Connections
sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf

# Change it to: Its already present just change 127.0.0.1 to 0.0.0.0
bind-address = 0.0.0.0

# Restart MySQL to Apply Changes
sudo systemctl restart mysql



MySQL Installation Link
bash <(curl -sL https://tinyurl.com/mr4brnzj) 




🚀 Docker Installation
Setup Docker on Ubuntu 24.04

📌 Docker Installation Steps
sudo apt update
sudo apt  install docker.io -y
sudo docker --version
sudo apt install docker-compose -y
docker-compose --version
                        



🚀 Maven Installation
Setup Maven on Ubuntu 24.04

📌 Maven Installation Steps
#  Switch to Root User
$ sudo su -

# Download Apache Maven 3.9.11
$ wget https://dlcdn.apache.org/maven/maven-3/3.9.11/binaries/apache-maven-3.9.11-bin.tar.gz

# Extract the Archive
$ tar -zxvf apache-maven-3.9.11-bin.tar.gz

# Remove the Tar File
$ rm -rf apache-maven-3.9.11-bin.tar.gz

# Rename the Extracted Directory
$ mv apache-maven-3.9.11 maven

# Add Maven to the PATH: Edit the .bashrc file:
$ vi ~/.bashrc

# Add this line at the end of the file:
$ export PATH=/root/maven/bin:$PATH

# Apply the Updated .bashrc
$ source ~/.bashrc

# Verify Maven Installation
$ mvn --version



Maven Installation Link
bash <(curl -sL https://tinyurl.com/52ykfnu5)




🚀 Tomcat Installation
Setup Tomcat on Ubuntu 24.04

📌 Tomcat Installation Steps
#  Switch to Root User
$ sudo su -

# Download Apache Tomcat v9.0.111
$ wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.111/bin/apache-tomcat-9.0.111.tar.gz

# Extract the Archive
$ tar -zxvf apache-tomcat-9.0.111.tar.gz

# Remove the Tar File
$ rm -rf apache-tomcat-9.0.111.tar.gz

# Confirgure Tomcat username admin & password admin
$ vi apache-tomcat-9.0.111/conf/tomcat-users.xml

# Configure Tomcat Remote Access
$ vi apache-tomcat-9.0.111/webapps/manager/META-INF/context.xml

# Start the Tomcat server
$ sh apache-tomcat-9.0.111/bin/startup.sh

# Shutdown the Tomcat server
$ sh apache-tomcat-9.0.111/bin/shutdown.sh
                        



Tomcat Installation Link
bash <(curl -sL https://tinyurl.com/mrhvupt9)



Jenkins Installation
Setup Jenkins on Ubuntu 24.04

Ubuntu 24.04 + 2gb RAM + 2 CPU + 10gb ROM
bash <(curl -sL https://tinyurl.com/2r6nkffn)




🚀 Prometheus Installation
Setup Prometheus on Ubuntu 24.04

Ubuntu 24.04 + 4gb RAM + 2 CPU + 20gb ROM
bash <(curl -sL https://tinyurl.com/57xn7sf8)





🚀 Node Exporter Installation
Setup Node Exporter on Ubuntu 24.04

Ubuntu 24.04 + 1gb RAM + 1 CPU + 8gb ROM
bash <(curl -sL https://tinyurl.com/ms6t4mwd)






🚀 Grafana Installation
Setup Grafana on Ubuntu 24.04

Ubuntu 24.04 + 4gb RAM + 2 CPU + 20gb ROM
bash <(curl -sL https://tinyurl.com/296t47pu)




                        
🚀 Ansible Installation
Setup Ansible on Ubuntu 24.04

Ansible Master node

bash <(curl -sL https://tinyurl.com/mse8n4k6)
                        
Run this only in Master Node
After this need to do manual steps to add Worker Nodes

Ansible Worker nodes

bash <(curl -sL https://tinyurl.com/munbkzpb)
                        
Run this in all the worker nodes




KubeAdm Cluster Installation
Setup Kubeadm Cluster on Ubuntu 24.04

Kube Master node

curl -sL https://tinyurl.com/mt346aen | bash
                        
Run this only in Master Node
After this need to do manual steps to add Worker Nodes
Kube Worker nodes

curl -sL https://tinyurl.com/yvmvxmzb | bash
                        
Run this in all the worker nodes









AWS CLI Installation
AWS CLI Installation in Ubuntu

AWS CLI Installation in Ubuntu
# 1. Update packages
sudo apt update

# 2. Install required packages
sudo apt install -y unzip curl

# 3. Download AWS CLI v2 installer
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

# 4. Unzip the installer
unzip awscliv2.zip

# 5. Run the installer
sudo ./aws/install

# 6. Check the version
aws --version
                        
AwsCli Installation Link
bash <(curl -sL https://tinyurl.com/4bcvxkz2)
                        




🚀 Nexus Repository Setup
Nexus Installation Link
Ubuntu 24.04 LTS + 4 GB RAM + 2 CPU + 20 GB Storage
bash <(curl -sL https://tinyurl.com/5an29335)
                
Add Nexus Repositories and Distribution Management





📌 Nexus Repositories in pom.xml
<repositories>
    <repository>
        <id>nexus-releases</id>
        <name>maven-releases</name>
        <url>http://localhost:8081/repository/maven-releases/</url>
    </repository>
    <repository>
        <id>nexus-snapshots</id>
        <name>maven-snapshots</name>
        <url>http://localhost:8081/repository/maven-snapshots/</url>
    </repository>
</repositories>
                          
<distributionManagement>
    <repository>
        <id>nexus-releases</id>
        <url>http://localhost:8081/repository/maven-releases/</url>
    </repository>
    <snapshotRepository>
        <id>nexus-snapshots</id>
        <url>http://localhost:8081/repository/maven-snapshots/</url>
    </snapshotRepository>
</distributionManagement>
                        




📌 Nexus Settings.xml
<settings>
    <servers>
        <server>
            <id>nexus-releases</id>
            <username>admin</username>
            <password>admin</password>
        </server>
        <server>
            <id>nexus-snapshots</id>
            <username>admin</username>
            <password>admin</password>
        </server>
    </servers>
</settings>
                        
