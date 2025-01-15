pipeline {
    agent any

       stages {
                stage('Build') {
            steps {
                echo 'Building the project with Maven...'
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests with Maven...'
                sh 'mvn test'
            }
        }
    }

