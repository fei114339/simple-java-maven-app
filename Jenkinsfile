
pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/fei114339/simple-java-maven-app'
                sh 'mvn -B -DskipTests clean package'
            }
        }
