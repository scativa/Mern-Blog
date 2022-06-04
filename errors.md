## Frontend
[Node.js v18.3.0 documentation - Common system errors](https://nodejs.org/api/errors.html#errors_common_system_errors)
> `ENOTFOUND` (DNS lookup failed): Indicates a DNS failure of either `EAI_NODATA` or `EAI_NONAME`. This is not a standard POSIX error.

```
[HPM] Error occurred while proxying request localhost:3000/story/getAllStories?search=&page=1 to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)
[HPM] Error occurred while proxying request localhost:3000/auth/private to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)  
```

```
PS > kubectl get all -o wide
NAME                                 READY   STATUS    RESTARTS   AGE   IP           NODE       NOMINATED NODE   READINESS GATES
pod/blog-backend-7f69859b69-6q48d    1/1     Running   0          6s    172.17.0.4   minikube   <none>           <none>
pod/blog-frontend-77c65f47c7-2xw8r   1/1     Running   0          5s    172.17.0.6   minikube   <none>           <none>
pod/blog-frontend-77c65f47c7-j5mcn   1/1     Running   0          5s    172.17.0.5   minikube   <none>           <none>
pod/mongo-d98bd4b68-9hlwg            1/1     Running   0          68s   172.17.0.3   minikube   <none>           <none>

NAME                    TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)        AGE   SELECTOR
service/blog-backend    ClusterIP   10.106.179.211   <none>        80/TCP         6s    app=blog-backend
service/blog-frontend   NodePort    10.99.38.180     <none>        80:30001/TCP   4s    app=blog-frontend
service/kubernetes      ClusterIP   10.96.0.1        <none>        443/TCP        21m   <none>
service/mongo           ClusterIP   10.97.196.159    <none>        80/TCP         65s   app=mongo

NAME                            READY   UP-TO-DATE   AVAILABLE   AGE   CONTAINERS      IMAGES                 SELECTOR
deployment.apps/blog-backend    1/1     1            1           6s    blog-backend    blog-backend:latest    app=blog-backend
deployment.apps/blog-frontend   2/2     2            2           5s    blog-frontend   blog-frontend:latest   app=blog-frontend
deployment.apps/mongo           1/1     1            1           69s   mongo           mongo:5.0.7            app=mongo

NAME                                       DESIRED   CURRENT   READY   AGE   CONTAINERS      IMAGES                 SELECTOR
replicaset.apps/blog-backend-7f69859b69    1         1         1       6s    blog-backend    blog-backend:latest    app=blog-backend,pod-template-hash=7f69859b69
replicaset.apps/blog-frontend-77c65f47c7   2         2         2       5s    blog-frontend   blog-frontend:latest   app=blog-frontend,pod-template-hash=77c65f47c7
replicaset.apps/mongo-d98bd4b68            1         1         1       69s   mongo           mongo:5.0.7            app=mongo,pod-template-hash=d98bd4b68
```

### Anexo - Frontend terminal
Comandos
```
cd Frontend
npm install
npm run start
```

Output
```
Compiled successfully!

You can now view frontend in the browser.

  Local:            http://localhost:3000
  On Your Network:  http://192.168.0.40:3000

Note that the development build is not optimized.
To create a production build, use npm run build.

asset static/js/bundle.js 13.6 MiB [emitted] (name: main) 1 related asset
asset index.html 1.38 KiB [emitted]
asset asset-manifest.json 190 bytes [emitted]
cached modules 11.9 MiB (javascript) 28.3 KiB (runtime) [cached] 243 modules
webpack 5.67.0 compiled successfully in 14920 ms
[HPM] Error occurred while proxying request localhost:3000/story/getAllStories?search=&page=1 to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)
[HPM] Error occurred while proxying request localhost:3000/auth/private to http://blog-backend:80/ [ENOTFOUND] (https://nodejs.org/api/errors.html#errors_common_system_errors)  
```


### Anexo - Backend terminal
Comandos
```
cd Backend
npm install
npm start
```


Output
```
npm WARN config global `--global`, `--local` are deprecated. Use `--location=global` instead.

up to date, audited 237 packages in 5s

22 packages are looking for funding
  run `npm fund` for details

4 vulnerabilities (3 high, 1 critical)

To address issues that do not require attention, run:
  npm audit fix

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
npm WARN config global `--global`, `--local` are deprecated. Use `--location=global` instead.

> backend@1.0.0 start
> nodemon server.js  

[nodemon] 2.0.15
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting `node server.js`
{
  CUDA_PATH: 'C:\\Program Files\\NVIDIA GPU Computing Toolkit\\CUDA\\v11.3',
  CUDA_PATH_V11_3: 'C:\\Program Files\\NVIDIA GPU Computing Toolkit\\CUDA\\v11.3',
  CUDA_PATH_V9_2: 'C:\\Program Files\\NVIDIA GPU Computing Toolkit\\CUDA\\v9.2',
  EMAIL_PASS: 'blblas',
  EMAIL_USERNAME: 'dummyusr@gmail.com',
  INIT_CWD: 'E:\\Proyectos\\Mern-Blog\\Backend',
  JWT_EXPIRE: '60m',
  JWT_SECRET_KEY: '-----BEGIN RSA PRIVATE KEY-----\n' +
    'Proc-Type: 4,ENCRYPTED\n' +
    '-----END RSA PRIVATE KEY-----',
  LIBTORCH_DIR: 'E:\\Repositories\\libtorch-win-shared-with-deps-debug-1.8.1+cu111',
  LOGONSERVER: '\\\\Z240NVIDIA',
  MONGO_URI: 'mongodb+srv://dummyusr:blaslllsas@cluster0.8zlru.mongodb.net/?retryWrites=true&w=majority',
  MOSQUITTO_DIR: 'E:\\Program Files\\mosquitto',
  NODE: 'C:\\Program Files\\nodejs\\node.exe',
  NODE_ENV: 'development',
  NODE_EXE: 'C:\\Program Files\\nodejs\\\\node.exe',
  NPM_CLI_JS: 'C:\\Program Files\\nodejs\\\\node_modules\\npm\\bin\\npm-cli.js',
  npm_command: 'start',
  npm_config_local_prefix: 'E:\\Proyectos\\Mern-Blog\\Backend',
  npm_config_noproxy: '',
  npm_config_prefix: 'C:\\Users\\Seba\\AppData\\Roaming\\npm',
  npm_config_userconfig: 'C:\\Users\\Seba\\.npmrc',
  npm_config_user_agent: 'npm/8.11.0 node/v16.15.1 win32 x64 workspaces/false',
  npm_lifecycle_event: 'start',
  npm_lifecycle_script: 'nodemon server.js ',
  npm_node_execpath: 'C:\\Program Files\\nodejs\\node.exe',
  npm_package_json: 'E:\\Proyectos\\Mern-Blog\\Backend\\package.json',
  npm_package_name: 'backend',
  npm_package_version: '1.0.0',
  NVCUDASAMPLES11_3_ROOT: 'C:\\ProgramData\\NVIDIA Corporation\\CUDA Samples\\v11.3',
  NVCUDASAMPLES9_2_ROOT: 'C:\\ProgramData\\NVIDIA Corporation\\CUDA Samples\\v9.2',
  NVCUDASAMPLES_ROOT: 'C:\\ProgramData\\NVIDIA Corporation\\CUDA Samples\\v11.3',
  NVTOOLSEXT_PATH: 'C:\\Program Files\\NVIDIA Corporation\\NvToolsExt\\',
  OPENCV_DIR: 'C:\\opencv-4.4.0',
  OS: 'Windows_NT',
  PORT: '5000',
  PROCESSOR_ARCHITECTURE: 'AMD64',
  PROCESSOR_IDENTIFIER: 'Intel64 Family 6 Model 158 Stepping 9, GenuineIntel',
  PROCESSOR_LEVEL: '6',
  RESET_PASSWORD_EXPIRE: '3600000',
  SESSIONNAME: 'Console',
  SMTP_HOST: 'smtp.gmail.com',
  SMTP_PORT: '587',
  TERM_PROGRAM: 'vscode',
  TERM_PROGRAM_VERSION: '1.67.2',
  URI: 'http://localhost:3000',
  VBOX_MSI_INSTALL_PATH: 'C:\\Program Files\\Oracle\\VirtualBox\\',
  windir: 'C:\\WINDOWS'
}
Server running on port  5000 : development
MongoDB Connection Successfully
```
