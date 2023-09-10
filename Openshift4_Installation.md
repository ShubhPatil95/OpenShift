## Openshift 4 Installation
## 1. Install Docker Desktop (install WSL2 as well)
- go to power shell or any other terminal and run below command, if output says "Hello from Docker!" then Docker is successfully installed on your system
  ```ruby
   docker run hello-world
  ```
## 2. Openshift4 Installation
There are 2 ways to install openshift and we will go with Openshift Developer Sandbox
- #### 1. Local Installation
  - No compatible with apple processors and windos home
  - High resouce requirnments(ram:9GB, storage:35GB, vCPUs:4)
- #### 2. Openshift Developer Sandbox
   - Online hosted installation
   - low resource requirnment
   - compatible with most operating systems
   - but keep in mind that you will need new cluster every 30 days
 
## 3. Installtion of Openshift Developer Sandbox
- go to link: https://developers.redhat.com/developer-sandbox
- click start your sandbox free
- login or create account and proceed further
- again click on start your sandbox on next page click DevSandbox
- Now you are at openshift-console page(this is very important page keep it open)
- ### Install OC(Opensfhit CLI)
- if you are already on openshift console then clikc '?' at top right of page and click "commad line tools"
- search and click "Download oc for Windows for x86_64" and donwload zip file
- once zip is downloaded, extract to folder name oc-folder under user home directory and copy the path of oc-folder
- then add this oc-folder path to environment variable PATH
- go to powershell or any shell and type oc, if documentation open ups then you have oc installed well configured on system

## 4. login to openshift4 cluster(hosted in sandbox)
- on openshift4 console page, clikc right top on your username and "copy login command"
- on new page click DevSandbox => display token => copy command under "Log in with this token"
- paste this command to powershell or any other shell
