1. EFS add AMAZON_EFS_CSI_DRIVER into IAM role
- kubectl create secret generic mysql-pass --from-literal=password=eks-mysql-pw 
2. kubectl apply -k "github.com/kubernetes-sigs/aws-efs-csi-driver/deploy/kubernetes/overlays/stable/?ref=release-1.3"
3. kubectl apply -f .\storage-config\efs-csi-node-sa.yaml
4. kubectl apply -f .\storage-config\efs-csi-node-sa-token.yaml
5. kubectl apply -f .\wordpress-efs\\*.yaml

