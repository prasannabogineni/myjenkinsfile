pipeline {

    agent any

    stages {

        stage('Git Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/prasannabogineni/war-web-project.git'
            }
        }
    }

    post {
        success {
            echo 'Git Clone Successful!'
        }

        failure {
            echo 'Git Clone Failed!'
        }
    }
}
