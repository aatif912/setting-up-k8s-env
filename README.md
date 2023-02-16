# setting-up-k8s-env in local windows machine

step 0 - Enable WSL Reference - https://www.ssl.com/how-to/enable-linux-subsystem-install-ubuntu-windows-10/

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

verification: `k version`

`![image](https://user-images.githubusercontent.com/13832737/219463880-08cd78e2-4289-479e-8b79-bc69979eb94b.png)
