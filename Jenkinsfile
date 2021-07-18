//Declarative Pipeline

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echow 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    
    post {
        success {
            mail to: 'eliasadriano2010@gmail.com.com',
             subject: "Success Pipeline: ${currentBuild.fullDisplayName}",
             body: "Everything is good with ${env.BUILD_URL}"
        }
        
        failure {
            mail to: 'eliasadriano2010@gmail.com.com',
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Something is wrong with ${env.BUILD_URL}"
        }
    }
    
    
    
    
    
    
    
}
