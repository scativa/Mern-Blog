mongodb+srv://seba:<password>@cluster0.yu4pr.mongodb.net/?retryWrites=true&w=majority

const { MongoClient, ServerApiVersion } = require('mongodb');
const uri = "mongodb+srv://seba:<password>@cluster0.yu4pr.mongodb.net/?retryWrites=true&w=majority";
const client = new MongoClient(uri, { useNewUrlParser: true, useUnifiedTopology: true, serverApi: ServerApiVersion.v1 });
client.connect(err => {
  const collection = client.db("test").collection("devices");
  // perform actions on the collection object
  client.close();
});


# En windows 10

## Administrador PowerShell
´´´
Windows PowerShell
Copyright (C) Microsoft Corporation. Todos los derechos reservados.
                                                                                                                        Prueba la nueva tecnología PowerShell multiplataforma https://aka.ms/pscore6                                                                                                                                                                    PS C:\WINDOWS\system32> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All                                                                                                                                               
Path          :
Online        : True
RestartNeeded : False



PS C:\WINDOWS\system32> minikube start --driver=hyperv
* minikube v1.25.2 en Microsoft Windows 10 Pro For Workstations 10.0.19043 Build 19043
* Using the hyperv driver based on user configuration
* Starting control plane node minikube in cluster minikube
* Creando hyperv VM (CPUs=2, Memory=4000MB, Disk=20000MB) ...
* Preparando Kubernetes v1.23.3 en Docker 20.10.12...
  - kubelet.housekeeping-interval=5m
  - Generando certificados y llaves
  - Iniciando plano de control
  - Configurando reglas RBAC...
* Verifying Kubernetes components...
  - Using image gcr.io/k8s-minikube/storage-provisioner:v5
* Complementos habilitados: storage-provisioner, default-storageclass

! C:\Program Files\Docker\Docker\resources\bin\kubectl.exe is version 1.21.2, which may have incompatibilites with Kubernetes 1.23.3.
  - Want kubectl v1.23.3? Try 'minikube kubectl -- get pods -A'
* Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
PS C:\WINDOWS\system32> minikube kubectl -- get po -A
NAMESPACE     NAME                               READY   STATUS    RESTARTS   AGE
kube-system   coredns-64897985d-rkjmk            1/1     Running   0          17s
kube-system   etcd-minikube                      1/1     Running   0          30s
kube-system   kube-apiserver-minikube            1/1     Running   0          30s
kube-system   kube-controller-manager-minikube   1/1     Running   0          30s
kube-system   kube-proxy-cnxxq                   1/1     Running   0          17s
kube-system   kube-scheduler-minikube            1/1     Running   0          30s
kube-system   storage-provisioner                1/1     Running   0          28s
PS C:\WINDOWS\system32> minikube dashboard
* Habilitando dashboard
  - Using image kubernetesui/dashboard:v2.3.1
  - Using image kubernetesui/metrics-scraper:v1.0.7
* Verifying dashboard health ...
* Launching proxy ...
* Verifying proxy health ...
* Opening http://127.0.0.1:64395/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/ in your default browser...
´´´


## VC terminal
### Frontend
´´´
...
webpack 5.67.0 compiled with 1 warning in 8672 ms
[HPM] Error occurred while proxying request localhost:3000/story/getAllStories?search=&page=1 to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)
[HPM] Error occurred while proxying request localhost:3000/auth/private to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)
[HPM] Error occurred while proxying request localhost:3000/auth/private to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)
´´´

### Backend
´´´
...
  URI: 'http://localhost:3000',
  USERDOMAIN: 'Z240NVIDIA',
  USERDOMAIN_ROAMINGPROFILE: 'Z240NVIDIA',
  USERNAME: 'Seba',
  USERPROFILE: 'C:\\Users\\Seba',
  VBOX_MSI_INSTALL_PATH: 'C:\\Program Files\\Oracle\\VirtualBox\\',
  VS140COMNTOOLS: 'C:\\Program Files (x86)\\Microsoft Visual Studio 14.0\\Common7\\Tools\\',
  VSCODE_GIT_ASKPASS_EXTRA_ARGS: '--ms-enable-electron-run-as-node',
  VSCODE_GIT_ASKPASS_MAIN: 'c:\\Users\\Seba\\AppData\\Local\\Programs\\Microsoft VS Code\\resources\\app\\extensions\\git\\dist\\askpass-main.js',
  VSCODE_GIT_ASKPASS_NODE: 'C:\\Users\\Seba\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe',
  VSCODE_GIT_IPC_HANDLE: '\\\\.\\pipe\\vscode-git-6d8e6b5f12-sock',
  windir: 'C:\\WINDOWS',
  WSLENV: 'WT_SESSION::WT_PROFILE_ID',
  WT_PROFILE_ID: '{61c54bbd-c2c6-5271-96e7-009a87ff44bf}',
  WT_SESSION: '7a0de153-a69d-48a6-b014-cc61e028ee29'
}
Server running on port  5000 : development
MongoDB Connection Successfully
´´´

## Problemas
No está levantado el docker

´´´
PS > docker build -t blog-backend Backend/
error during connect: This error may indicate that the docker daemon is not running.: Post "http://%2F%2F.%2Fpipe%2Fdocker_engine/v1.24/build?buildargs=%7B%7D&cachefrom=%5B%5D&cgroupparent=&cpuperiod=0&cpuquota=0&cpusetcpus=&cpusetmems=&cpushares=0&dockerfile=Dockerfile&labels=%7B%7D&memory=0&memswap=0&networkmode=default&rm=1&shmsize=0&t=blog-backend&target=&ulimits=null&version=1": open //./pipe/docker_engine: The system cannot find the file specified.
PS > docker build -t blog-frontend Frontend/
error during connect: This error may indicate that the docker daemon is not running.: Post "http://%2F%2F.%2Fpipe%2Fdocker_engine/v1.24/build?buildargs=%7B%7D&cachefrom=%5B%5D&cgroupparent=&cpuperiod=0&cpuquota=0&cpusetcpus=&cpusetmems=&cpushares=0&dockerfile=Dockerfile&labels=%7B%7D&memory=0&memswap=0&networkmode=default&rm=1&shmsize=0&t=blog-frontend&target=&ulimits=null&version=1": open //./pipe/docker_engine: The system cannot find the file specified.
´´´

services.msc
[Docker daemon is not running – Resolution 1: Restart Docker service](https://www.thecodebuzz.com/docker-error-daemon-is-not-running/#:~:text=Docker%20daemon%20is%20not%20running%20%E2%80%93%20Resolution%201%3A%20Restart%20Docker%20service,service%20will%20resolve%20the%20error.)



