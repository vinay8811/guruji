pipeline {
    agent any
    environment {
        PATH = "/root/maven/bin:$PATH"
    }
    stages {
        stage('build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
        stage('SonarQube analysis') {
            environment {
                scannerHome = tool 'vinay-sonar-scanner'
            }
            steps {
                withSonarQubeEnv('vinay_sonarqube_server') {
                    sh "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
    }
}

