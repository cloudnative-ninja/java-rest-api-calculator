pipeline{
    agent any
    stages{
        stage('Build the code'){
            steps{
                sh 'mvnw clean compile'
            }
        }
        stage('Test the code'){
            steps{
                sh 'mvnw test'
            }
        }
    }    
    post{
        always{
            junit '**/target/surefire-reports/TEST-*.xml'
        }
    }
}
