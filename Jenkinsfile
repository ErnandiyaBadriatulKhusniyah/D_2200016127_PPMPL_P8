pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ErnandiyaBadriatulKhusniyah/D_2200016127_PPMPL_P8.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run Unit Tests') {
            steps {
                bat 'npm test'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add build commands here if needed (e.g., MSBuild, npm run build, etc.)
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deploy commands here if needed
            }
        }
    }
    post {
        success {
            echo 'Pipeline finished successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}