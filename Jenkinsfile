pipeline {

    agent any

    environment {
        PATH = "/opt/maven/bin:$PATH"
    }

    stages {

        stage('Git Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/prasannabogineni/war-web-project.git'
            }
        }

        stage('Maven Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo 'Git Clone and Maven Build Successful!'
        }

        failure {
            echo 'Git Clone or Maven Build Failed!'
        }
    }
}
