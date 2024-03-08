pipeline {
    agent any
    environment {
    }

    stages {
        stage('build') {
            steps{
                echo 'Building...'
            }
            post {
                always {
                    jiraSendBuildInfo site: 'hiuhuyn.atlassian.net'
                }
            }
        }
        stage('deploy'){
            steps{
                echo 'Deploying...'
            }
            post {
                always {
                    jiraSendDeploymentInfo environmentId: 'DOCACICD-2'
                }
            }
        }
    }
    
}
