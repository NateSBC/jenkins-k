pipeline{ 
    agent any 
        stages{ 
            stage("k8s"){ 
                steps{ 
                    withKubeCredentials(kubectlCredentials: [[caCertificate: '', clusterName: 'newcluster', contextName: '', credentialsId: 'jenkins-k', namespace: 'default', serverUrl: 'https://0B67A1F4AA9754B057A4326569B66095.gr7.eu-west-2.eks.amazonaws.com';]]) 
                    { 
                    sh 'curl -LO "https://storage.googleapis.com/kubernetes-release/release/v1.20.5/bin/linux/amd64/kubectl"'; 
                    sh 'chmod u+x ./kubectl' 
                    sh './kubectl get nodes' 
                    sh './kubectl create -f pod.yaml' 
                    sh './kubectl get pods' 
                    } 
                }    
        } 
    } 
} 
