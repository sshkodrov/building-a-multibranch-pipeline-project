pipeline {
    agent {
        label 'django' 
    }
    stages {
        stage('Install Helm Chart') {
            steps {
                script {
            
                    sh 'helm upgrade --install my-release ./simple-helm --namespace default '
                }
            }
        }
    }
}
