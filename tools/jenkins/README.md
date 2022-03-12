kubectl create namespace jenkins
helm repo add jenkinsci https://charts.jenkins.io
helm repo update

chart=jenkinsci/jenkins
helm install jenkins -n jenkins -f values.yaml $chart