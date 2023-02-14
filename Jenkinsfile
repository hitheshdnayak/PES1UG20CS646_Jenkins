pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS646 sample.cpp'
                build job: 'PES1UG20CSwg646-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS646'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
