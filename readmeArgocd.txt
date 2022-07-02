1. Install argoCD (https://www.youtube.com/watch?v=MeU5_k9ssrs&t=1868s )
  kubectl create namespace argocd
  kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

kubectl get namespaces

kubectl config get-contexts

kubectl config set-context argocd --namespace=argocd --cluster=minikube --user=minikube

kubectl config use-context argocd 
kubectl config use-context minikube
kubectl config use-context kong 
kubectl config use-context development


2. argoCD Starting GUI

kubectl port-forward service/argocd-server 8085:443 -n argocd

localhost:8085 -> OK 
user admin 
kubectl get secret argocd-initial-admin-secret  -o yaml -n argocd


UDRXR1dva2M4bnRMRTByYQ==

[System.Text.Encoding]::Ascii.GetString([System.Convert]::FromBase64String("UDRXR1dva2M4bnRMRTByYQ=="))  
P4WGWokc8ntLE0ra

ca fonctionne pour avoir le pwd 


application.yaml c'est ce qui defini lelien entre argcode et Git  il faut le faire a la main 
main on le met quand meme dans GIT 


cd  D:\Kubernetes\Infrastructure\argocd


kubectl apply -f .\application.yaml
et tout fonctionne 

----------------------------------------------------------------------------

cd argocd 
git remote add origin https://gitlab.com/vincentparisi/development.git
git branch -M main
git push -uf origin main


git config --global user.name "vincentparisi"
git config --global user.email "vincentparisi@gmail.com"
Git210659@

172.26.171.55=
