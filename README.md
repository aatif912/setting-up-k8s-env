# setting-up-k8s-env in local windows machine

step 0 - Enable WSL on windows machine.
Reference - https://www.ssl.com/how-to/enable-linux-subsystem-install-ubuntu-windows-10/

open bash terminal where repo is cloned. Repo link - https://github.com/aatif912/k8s-voting-app

![image](https://user-images.githubusercontent.com/13832737/219461184-2b780de9-4119-4e21-90de-af40ff97747e.png)

Download kubectl - 
https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

`curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"`

`curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"`

`sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl`

`chmod +x kubectl`

`mkdir -p ~/.local/bin`

`mv ./kubectl ~/.local/bin/kubectl`

`##### and then append (or prepend) ~/.local/bin to $PATH`

![image](https://user-images.githubusercontent.com/13832737/219462509-872c5e76-3669-4f35-9895-3ed8412aab0d.png)

Setting up alias 

`alias k='kubectl'`

`alias c='clear'`

![image](https://user-images.githubusercontent.com/13832737/219470171-30dac50b-d7c2-41d3-a5b7-d43f8595d11e.png)


verification: `k version`

`![image](https://user-images.githubusercontent.com/13832737/219463880-08cd78e2-4289-479e-8b79-bc69979eb94b.png)
![image](https://user-images.githubusercontent.com/13832737/219464878-e0daa1a2-7f97-42b8-ae10-4eee557a2160.png)

![Uploading image.png…]()


install az-cli:  `curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash`
![image](https://user-images.githubusercontent.com/13832737/219466390-2dfbb095-e08e-4572-abbb-3bcb759ad6d8.png)

Install kubectl locally using the az aks install-cli command: `az aks install-cli`

Reference: https://learn.microsoft.com/en-us/azure/aks/learn/quick-kubernetes-deploy-cli
![image](https://user-images.githubusercontent.com/13832737/219466845-f887e693-00ea-4279-a221-118d0b4de0f6.png)

verification:

![image](https://user-images.githubusercontent.com/13832737/219469704-4c44409c-3555-4c45-ba17-2500838d40ac.png)
