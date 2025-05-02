# settingup-aMinikube
Here I will be submiting my project on setting up a minikube 

# OVERVIEW
This project is about Kubernetes and how it works. it is about how to set up Minikubes. 

## PURPOSE OF THIS PROJECT
1. Gain a comprehensive understanding of Kubernetes and its fundamental concepts
2. master the use of minikubes on local Kubernete cluster deploymebts and experimentation 
3. Acquired hands on experience with docker and understand containerization principles and how to create, manage and distribute containerized aplications 
4. built and deployed applications on minikube. 


## Installing Minikube on Linux 

### Step 1 -REFRESH THE PACKAGE LIST ON THE DEBIAN-BASED SYSTEM
 The first step is to refresh the package list on the Debian-based system, ensuring the latest software information is available for installation. 
This is done by using the code "Sudo apt-get update"
![1img](./1img.png)

### Step 2 -INSTALL ESSENTIAL PACKAGES 
The next step is to run a linux command that installs essential packages including certificate authorities, a data transfer tool (curl), and the GNU Privacy Guard for secure communication and package verification. 
the Command to run is "sudo apt-get install ca-certificate curl gnupg"
![2img](./2img.png)

### Step 3 -CREATE A DIRECTORY WITH SPECIFIC PERMISSION
The Next step is to run a command that would create a directory (/etc/apt/keyrings) with specific permissions (0755) for storing keyring files which are used for dockers authentication. 

The command is "sudo install -m 0755 -d /etc/apt/keyrings

the image below depicts this 
![3img](./3img.png)

### Step 4 -DOWNLOAD THE DOCKER GPG KEY USING CURL
The next step 
the next step is to download the Docker GPG Key using curl
the command below depicts this
"curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
the image below depicts this 
![4img](./4img.png)
this simply means My system has Docker's trusted key saved in the correct folder.
Later, when I install Docker, my system will trust the packages because the signature will match this key. 

### Step 5 -SET READ PERMISSION FOR ALL USERS OF DOCKER GPG KEY FILE WITHIN THE APT KEYRING DIRECTORY
The next step is to set read permission for all users of docker GPG key file within the APT keyring directory. this is done using the command below "sudo chmod a+r /etc/apt/keyrings/docker.gpg"
the image below depicts this 
![5img](./5img.png)

### Step 6 -RUN THE ECHO COMMAND WHICH CREATES A DOCKER APT REPOSITORY CONFIGURATION ENTRY FOR THE UBUNTU SYSTEM
the next step is to run the echo command which creates a Docker APT repository configuration entry for the ubuntu system, incorporating the system architecture and Docker GPG Key and then "sudo tee /etc/apt/sources.list.d /docker.list>/dev/null" writes the configuration to the "/etc/apt/sources.list.d/docker.list" file. 

the image below depicts this 
![6img](./6img.png)

### Step 7 -INSTALL THE LATEST VERSION OF DOCKER 

After all these are done, the next step is to install the latest version of docker and this is done using the command "sudo apt-get update"
the image below depicts that
![7img](./7img.png)
![8img](./8img.png)

### Step 8 -VERIFY THAT DOCKER HAS BEING SUCCESSFULLY INSTALLED
the next step is to verify that docker has being successfully installed. this is done by running this command "sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin"

the image below depicts this 
![9img](./9img.png)

### Step 9 -VERIFY THAT EVERYTHING IS RUNNING WELL
The next step is to verify everything is running well and this is done by running the command below 
"sudo systemctl status docker"

the image below depicts this
![10img](./10img.png)

### Step 10 -INSTALL THE MINIKUBE 
The next thing is install the minikube and this is done by running the command below 
"curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb"
the image below depicts this. 
![11img](./11img.png)

### Step 11 -DOWNLOAD MINIKUBES BINARY AND INSTALL MINIKUBE 
once this is done the next step is to download minikubes binary and install minikube using dpkg. the comand is "sudo dpkg -i minikube_latest_amd64.deb"

the image below depicts this. 
![12img](./12img.png)

### Step 12 -START MINIKUBE
The next thing to do is to start the minikube using this command "minikube start --driver=docker"
the image below depiocts this 
![13img](./13img.png)
![14img](./14img.png)
![15img](./15img.png)
![16img](./16img.png)
![17img](./17img.png)
![18img](./18img.png)
![19img](./19img.png)
![20img](./20img.png)

### Step 13 -DOWNLOAD KUBERNETES COMMAND LINE TOOL
The next thing is to note that Kubectl is the command line interface tool for interacting with and managing kubernetes clusters allowing me to deploy, inspect and manage applications within he kubernetes enviroment. this command "sudo snap install kubectl --classic" will download the kubernetes command line (kubectl) tool to interact with kubernetes cluster. the image below depicts this ![21img](./21img.png)

## CONCLUSION
I gained a comprehensive understanding of Kubernetes and its fundamental concepts. Running each command and studying each command to understand how it works. I also mastered the use of minikubes on local Kubernete cluster deploymebts and experimentation and acquired hands on experience with docker and understand containerization principles and how to create, manage and distribute containerized aplications. through this project, I have built and deployed applications on minikube. 

