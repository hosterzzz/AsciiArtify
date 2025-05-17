Getting access WEB UI:

after Argosd installed put:

Check if AdgoCD working correct:
#kubectl get all -n argocd
#kubectl get po -n argocd -w

Check create secrets
#kubectl get secrets -n argocd
#kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d ;echo

Port forward to Web UI
#kubectl port-forward svc/argocd-server -n argocd 8080:443

create Application (example on demon)

Check logs
#kubectl logs -n <namespace> <podname>
