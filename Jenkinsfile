pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
              
                bat "git clone https://github.com/lakshmiKrishnaa/maven-samples-master.git"
                bat "mvn clean -f maven-samples-master"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f maven-samples-master"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f maven-samples-master"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f maven-samples-master"
            }
        }
    }
}
