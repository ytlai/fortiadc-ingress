
# Fortiadc Ingress Controller

# Deployment

## Get Repo Information
   

    helm repo add fortiadc-ingress-controller https://ytlai.github.io/fortiadc-ingress/

    helm repo update

   ## Install FortiADC Ingress Controller
   :warning: Before install, you have to create the image pull secret under the specified namespace fortiadc-ingress.

    helm install first-release --namespace fortiadc-ingress fortiadc-ingress-controller/fadc-k8s-ctrl

## Check the installation

    helm history -n fortiadc-ingress first-release
    
    kubectl get -n fortiadc-ingress deployments
    
    kubectl get -n fortiadc-ingress pods
 
## Upgrading chart

    helm repo update
    helm upgrade -n fortiadc-ingress first-release fortiadc-ingress-controller/fadc-k8s-ctrl

## Uninstall Chart

    helm uninstall -n fortiadc-ingress first-release
