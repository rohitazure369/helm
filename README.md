# helm

how to install helm in Ubunut...
curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
sudo apt-get install apt-transport-https --yes


echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list

sudo apt-get update
sudo apt-get install helm

git clone https://github.com/rohitazure369/helm
cd helm

# how to run it...

kubectl get ns

helm install webapp1 ./webapp1 -n dev --create-namespace -f dev.yaml


#
kubectl get all -n dev

helm install webapp1 ./webapp1 -n prod --create-namespace -f prod.yaml

#
kubectl get all -n prod

helm list --all-namespaces

helm uninstall webapp -n dev
helm uninstall webapp -n prod 

kubectl get ns












