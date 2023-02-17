pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output New.cpp'
                build job : 'PES1UG20CS641-1'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
