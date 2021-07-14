pipeline{
    agent any
    stages{
        stage('Build the code'){
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('Test the code'){
            steps{
                sh 'mvn test'
            }
        }
    }    
    post{
        always{
            junit '**/target/surefire-reports/TEST-*.xml'
        }
    }
}
