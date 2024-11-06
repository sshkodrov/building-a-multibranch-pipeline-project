pipeline {
    agent {
        label 'slave' 
    }
    stages {
        stage('Install Helm Chart') {
            steps {
                script {
            
                    sh 'helm install my-release ./simple-helm'
                }
            }
        }
    }
}
