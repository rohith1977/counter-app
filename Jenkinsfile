pipeline {
    agent any

    stages {
        stage('Git Checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/rohith1977/counter-app.git'
            }
        }
        stage('Maven Unit Testing'){
            steps {
                sh 'mvn test'
            }
        }
        stage('Integration Testing'){
            steps {
                sh 'mvn verify -DskipUnitTests'
            }
        }
    }
}