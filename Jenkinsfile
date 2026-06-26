pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/Sandeep-Namburu/DevOps-labs.git',
                    credentialsId: 'github-pat'
            }
        }
        stage('Build') {
            steps {
                echo 'Triggered by GitHub push!'
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                echo "Deploying to Nginx web root..."
                cp app.txt /usr/share/nginx/html/
                '''
            }
        }
    }
}
