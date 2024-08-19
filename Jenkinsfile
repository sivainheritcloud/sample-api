pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git url: 'https://github.com/sivainheritcloud/sample-api.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Run Maven build
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run Maven tests
                sh 'mvn test'
            }
        }
    }

    post {
        success {
            echo 'Build and test stages completed successfully!'
        }
        failure {
            echo 'Build or test failed.'
        }
    }
}
