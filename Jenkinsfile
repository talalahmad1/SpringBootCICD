pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                #sh './gradlew clean build'
                sh 'gradle assemble'
            }
        }
         stage('Test') {
            steps {
                #sh './gradlew test'
                sh 'gradle test'
            }
        }
        stage('Build Docker Image') {
            steps {
                #sh './gradlew docker'
                sh 'gradle docker'
            }
        }
        stage('Run Docker Image') {
            steps {
                #sh './gradlew dockerRun'
                sh 'gradle dockerRun'
            }
        }
    }
}
