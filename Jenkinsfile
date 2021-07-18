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
            emailext(
                subject: "${env.JOB_NAME} na build [${env.BUILD_NUMBER}] foi deployado com sucesso :D",
                body: "Verifique a saída da console do Job ${env.JOB_NAME} em [${env.BUILD_URL}] ",
                to: "eliasadriano2010@gmail.com"
            )
        }
        
        failure {
            emailext(
                subject: "${env.JOB_NAME} na build [${env.BUILD_NUMBER}] não pôde ser deployado",
                body: "Verifique a saída da console do Job ${env.JOB_NAME} em [${env.BUILD_URL}] ",
                to: "eliasadriano2010@gmail.com"
            )
        }
    }
    
    
    
    
    
    
    
}
