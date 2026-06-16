pipeline{
    agent any
    stages{
        stage('checkout'){
            steps { git 'http://github.com/repo.git' }
        }
        stage('Build'){
            steps { sh 'mvn clean package' }
        }
        stage('Test'){
            steps { sh 'mvn test' }
        }
    }
    post{
        always{
            junit 'target/surefile-reports/*.xml'
        }
    }
}