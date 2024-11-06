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
            
                    sh 'helm upgrade --install my-release oci://registry-1.docker.io/bitnamicharts/apache '
                }
            }
        }
    }

}