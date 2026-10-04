pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['development', 'testing', 'production'])
    }
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t employee-service-portal:$BUILD_NUMBER .'
            }
        }
        stage('Deploy') {
            steps { echo "Deploying to ${params.ENVIRONMENT}" }
        }
    }
}