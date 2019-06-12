pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
               bat "mvn clean"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test"
            }
        }
        stage('Deploy') {
            steps {
                bat "cf login -a api.run.pivotal.io -u mokemz24@gmail.com -p @MmZ119915\$"
                bat "cf push"
            }
        }
    }
}