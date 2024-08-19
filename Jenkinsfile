pipeline {
    agent any

    environment {
        JAVA_HOME = tool name: 'JDK 1.8', type: 'JDK'
        MAVEN_HOME = tool name: 'Maven 3.8.6', type: 'Maven'
        PATH = "${MAVEN_HOME}/bin:${JAVA_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git url: 'https://your-repo-url.git', branch: 'main'
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
