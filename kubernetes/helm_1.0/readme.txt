1. kubectl create -f rbac-tiller.yaml
2. helm init --service-account tiller --upgrade
3. helm install --name op-viride-acme couchbase/couchbase-operator
4. kubectl logs -f deployment/op-viride-acme-couchbase-operator --namespace default
5. kubectl logs -f deployment/OP-viride-acme-couchbase-admission-controller --namespace default
6. helm install --name cb-viride-acme couchbase/couchbase-cluster
