properties([parameters([choice(choices: ['Yes', 'No', 'Maybe', 'Sure'], description: 'Please choose your deploy something', name: 'Deploy?')])])
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                if(Deploy? == "Yes"){
                    echo 'Hello World'
                }
                sh 'echo hi'
            }
        }
        stage('Hello again') {
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
