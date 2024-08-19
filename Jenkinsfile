pipeline {
 agent any
 stages {
 stage('Build') {
 steps {
 echo "build success"
 bat "mvn clean install"
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
}
