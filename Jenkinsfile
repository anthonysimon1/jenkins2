pipeline {
        agent {
                docker {
                        image 'node:6-alpine'
                        args '-p 3000:3000'
                }
        }
        environment {
            CI = 'true'
        }
        stages {
            stage('Build') {
                steps {
                    sh 'npm install'
                }
            }
            stage('Test') {
                steps {
                    sh './jenkins2/src/__tests__/App.test.js'
                }
            }
        }
}