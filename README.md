**PHP Application with a Redis Backend**
    To Deploy to an already created K8s cluster: 
    #create the redis master deployment
    kubectl create -f redis-master.yaml
    #create the redis master svc
    kubectl create -f redis-master-svc.yaml
    #create the redis slave deployment
    kubectl create -f redis-slave.yaml

    #create the redis slave svc
    kubectl create -f redis-slave-svc.yaml

    #create php frontend deployment
    kubectl create -f guestbook-frontend.yaml

    #create php frontend service
    kubectl create -f guestbook-frontend-svc.yaml

    #check everything deployed so far
    kubectl get svc
