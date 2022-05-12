follow getting startet untill step 6

https://argo-cd.readthedocs.io/en/stable/getting_started/


---

create the deployment for the aplication(borrowed from the original repo)

---

gen key
ssh-keygen -t ed25519 -C "elieser.pereira@container-solutions.com" -f argotest

add repo 

argocd repo add git@github.com:elieser1101/cre-labs-microservices-demo.git --ssh-private-key-path /home/us1/containersol/cre-labs-microservices-demo/argocd/argotest

---

argocd app create emailservice --repo git@github.com:elieser1101/cre-labs-microservices-demo.git --path argocd --dest-server https://kubernetes.default.svc --dest-namespace default
