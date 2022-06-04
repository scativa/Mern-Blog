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
