pipeline {
    agent any 

    stages  {
        stage('Checkout'){
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps{
                sh 'mvn clean package'
            }
        
        }
        stage('Test') {
            steps{
                sh 'mvn test'
            }

        }
    }

    post {

            success {
                echo 'Build and tests passed!'
            }
            failure {
                echo 'Build failed.'
            }
    }
}
