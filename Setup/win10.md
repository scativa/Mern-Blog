# Setup in Win10

## Minikube

### VirtualBox
No corre si la PC está en modo Hiper-v

### Hiper-V
```
minikube start --driver=hyperv
```
Precisa privilegios de administrados o agregar al usuario al grupo "_hyper-v administrators_"

Solución:
["Hyper-v commands have to be run as an Administrator" in minikube when running as Administrator - Stackoverflow.com](https://stackoverflow.com/questions/64209557/hyper-v-commands-have-to-be-run-as-an-administrator-in-minikube-when-running-a)
- Right-clicked on "This PC" and selected "Manage."
- Found my user inside of "Local Users and Groups" -> "Users."
- Opened my user's properties.
-  the "Member Of" tab, I clicked "Add" and entered "hyper-v administrators."
- "Check Names" ensured that I had it spelled correctly.


