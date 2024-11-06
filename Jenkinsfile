pipeline {
    agent {
        label 'django' 
    }
     stages {
        stage('Checkout SCM') {
            steps {
                    checkout scm
            
                    
            }
        }
        stage('Install Helm Chart') {
            steps {
                script {
            
                    sh 'helm upgrade --install my-release ./simple-helm '
                  
                }
            }
        }
        stage('Port Forward'){
            steps{
                 sh 'kubectl port-forward service/apache-service 8080:80'
            }
        }
    }

}