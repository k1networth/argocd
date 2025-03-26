# argocd

helm install app app-helm-chart/ -n my-namespace

---

kubectl patch svc argocd-server -n my-namespace -p '{"spec": {"type": "LoadBalancer"}}'

---

kubectl -n my-namespace get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
