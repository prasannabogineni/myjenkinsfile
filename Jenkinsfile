pipeline {

    agent any

    stages {

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Check WAR') {
            steps {
                sh 'ls -lh target/*.war'
            }
        }
    }

    post {

        success {
            echo 'BUILD SUCCESSFUL - WAR FILE CREATED!'
        }

        failure {
            echo 'BUILD FAILED!'
        }
    }
}
