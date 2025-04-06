# ClusterRole-ClusterRoleBinding

🎯 Goal:
Grant john read-only access to cluster-level resources like nodes, namespaces, and persistentvolumes.
✅ 1. Create the ClusterRole
✅ 2. Create the ClusterRoleBinding
💡 Apply with kubectl:
kubectl apply -f clusterrole-john-reader.yaml
kubectl apply -f clusterrolebinding-john.yaml

🧪 Test with John's context:
Switch to John's context and try cluster-level access:
kubectl config use-context john-context

kubectl get nodes
kubectl get namespaces
kubectl get pv
He should be able to read but not modify these resources.


