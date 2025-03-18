pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS680-1'
                    sh 'gcc -o dogesh PES1UG22CS680.cpp' //oh no I am stupid
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
