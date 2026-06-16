pipeline{
    agent any
    stages{
        stage('checkout'){
            steps { git url: 'http://github.com/anishudupan-rns/devops-pgrm7.git', branch:'main' }
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
            junit 'target/surefire-reports/*.xml'
        }
    }
}
