pipeline {

    agent any

    stages {

        stage('Git Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/prasannabogineni/war-web-project.git'
            }
        }

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
            echo '================================'
            echo 'BUILD SUCCESSFUL!'
            echo 'WAR file created successfully.'
            echo '================================'
        }

        failure {
            echo '================================'
            echo 'BUILD FAILED!'
            echo 'Check Jenkins console output.'
            echo '================================'
        }
    }
}
