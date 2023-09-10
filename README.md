imperative commands:

1. expose deployment
     k expose deploy my-webapp --type=NodePort --name=front-end-service --port=80 --dry-run=client -oyaml>q1.yaml

2. create ingress with rule
     kubectl create ingress ingress --rule="ckad-mock-exam-solution.com/video*=my-video-service:8080" --dry-run=client -oyaml > ingress.yaml

3. create pod:
     k run nginx1401 --image=nginx --namespace=default --dry-run=client -oyaml>q6.yaml

4. create pod 
     k run nginx-448839 --image nginx:alpine

5. create NameSpace
     k create ns apx-z993845

6. Deployment with replicas
     k create deploy httpd-frontend --image httpd:2.4-alpine --replicas 3

7. create pod with labels
     k run messaging --image redis:alpine --labels=tier=msg

8. create configmap
     k create configmap cm-3392845 --from-literal=DB_NAME=SQL3322 --from-literal=DB_HOST=sql322.mycompany.com --from-literal=DB_PORT=3306

9. create secret
     k create secret generic db-secret-xxdf --from-literal=DB_Host=sql01,    --from-literal=DB_User=root, --from-literal=DB_Password=password123

10. create deployment and expose deployment
     kubectl create deployment redis --image=redis:alpine --replicas=1
     kubectl expose deployment redis --name=redis --port=6379 --target-port=6379

11. Edit pod-deployment-service file:
     k edit pod pod-name 
     k edit deployment deployment-name
     k edit service service-name 
    

12. Once file is edit and changes are being save. now apply changes to update
     K replace --force -f q1.yaml 

13. Undo Rolling update deployment
     k rollout undo deployment nginx-deploy

14. Check networking working fine between pods and svc
     k exec -it webapp-color -- sh
     /opt # nc -v -z -w 2 secure-service 80

15.  