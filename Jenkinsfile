pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/your-username/CC_LAB-6.git'
            }
        }

        stage('Build Backend Image') {
            steps {
                script {
                    docker.build("backend-image", "./backend")
                }
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run backend-image'
            }
        }
    }
}
