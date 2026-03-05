pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/naganikhila9999-sudo/carweb-static.git'
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh '''
                sudo rm -rf /var/www/html/*
                sudo cp -r * /var/www/html/
                '''
            }
        }

    }

    post {
        success {
            echo 'Website deployed successfully!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
