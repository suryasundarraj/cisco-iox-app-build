# Cisco IOx Application building using Vagrant

## Recommeded Softwares to be installed: 

### Windows/ MAC Intel/ Linux: 
Git, Vagrant and Virtualbox 

### MAC ARM based - M1/M2/M3:
Git, Vagrant and VMWare Fusion 

# To build a custom app 

Step 1: Clone the repo 

`
git clone https://github.com/suryasundarraj/cisco-iox-app-build.git
`

Change the directory: 

`
cd cisco-iox-app-build/ioxappbuild
`

Step 2: Spin up the vagrant VM

`
vagrant up
`

Step 3: Copy your application to following directory **"cisco-iox-app-build/ioxappbuild"**

`
vagrant ssh
`

Ex: I have copied "app" folder to **"cisco-iox-app-build/ioxappbuild"** directory 

Step 4: Build the application using docker 

`
vagrant@vagrant:/vagrant/app$ docker build -t app .
`

<img width="1478" alt="image" src="https://github.com/user-attachments/assets/bb78bcc7-dbb0-4ead-a382-10a51a6a071e">

Step 5: Build the package to deploy 

`
vagrant@vagrant:/vagrant/app$ mkdir pkg
vagrant@vagrant:/vagrant/app$ ioxclient docker pkg app pkg/
`

Step 6: 

Once the application build is complete, the package.tar can be found under **"cisco-iox-app-build/ioxappbuild/app/pkg"**


<img width="987" alt="image" src="https://github.com/user-attachments/assets/6d22f283-5332-4e7c-944e-00411747db49">



