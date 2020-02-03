pipeline {
    agent any
    stages {
        stage('Compile stage') {
            steps {
           echo "Compile with Maven"
           sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo "Testing stage"
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo "test"
            }
        }
    }
     post {
            always {
                archive "target/**/*"
                junit 'target/surefire-reports/*.xml'
            }
        }
}