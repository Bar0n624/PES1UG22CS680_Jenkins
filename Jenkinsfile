pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS680-1'
                    sh 'g++ -o dogesh PES1UG22CS680.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './dogesh'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying ICMB!'
            }
        }
    }

    post {
        failure {
            echo 'Skill issue'
        }
    }
}
