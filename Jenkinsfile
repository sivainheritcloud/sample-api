pipeline {
 agent any
 stages {
 stage('Build') {
 steps {
 echo "build processing"
 bat "mvn clean install"
 }
 }
   stage('Test') {
            steps {
                echo 'Running tests...'
                // Run Maven tests
                bat "mvn test"
            }
        }
}
}
