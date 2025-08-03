pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'echo hi'
            }
        }

        stage('build docker image') {
            parallel {
                stage('firstBranch') {
                    steps {
                        sh 'python3 main.py'
                    }
                }
                stage('secondBranch') {
                    steps {
                        echo 'Hello from secondBranch'
                    }
                }
            }
        }

        stage('push to hub') {
            steps {
                echo 'Hello World'
                sh 'echo hi'
            }
        }
    }
}
