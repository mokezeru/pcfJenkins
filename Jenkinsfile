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
                        bat "mvn package"
                    }
                }
        stage('cf push') {
            steps {
                bat "cf login -a api.run.pivotal.io -u mokemz24@gmail.com -p @MmZ119915\$"
                bat "cf push pcfJenkins -p target/pcfJenkins.jar -b https://github.com/cloudfoundry/java-buildpack.git"
            }
        }
    }
}