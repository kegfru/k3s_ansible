# k3s_ansible

## Demo from
Ansible playbook for https://dev.to/kalaspuffar/creating-your-first-kubernetes-cluster-3kp2

## Modify
Edit `hosts` file with actual hosts, change vars if needed.

## Run
`ansible-playbook k3s_ansible/lan.yml -i k3s_ansible/hosts`

## Kubernetes Dashboard
https://hub.docker.com/r/kubernetesui/dashboard
1. Copy token from `kubectl -n kube-system describe secret admin-user`
2. Run `kubectl port-forward -n kubernetes-dashboard service/kubernetes-dashboard 10443:443 --address 0.0.0.0` from Master
3. Go to https://master-ip:10443 and authorize with token
