def flag = true

pipeline {
    agent any
    environment {
        NEW_VERSION = '1.3.0'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
            }
        }
        stage('Test') {
            when {
                expression {
                    flag == true
                }
            }
            steps {
                echo 'Testing Project'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project'
            }
        }
    }
    post {
        always {
            echo 'Post build condition running'
        }
        failure {
            echo 'Post Action if Build Failed'
        }
    }
}
