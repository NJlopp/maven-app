@Library('jenkins-shared-library') _

pipeline {
    agent any

    stages {
        stage('Build JAR') {
            steps {
                buildJar()
            }
        }

        stage('Docker Login') {
            steps {
                dockerLogin()
            }
        }

        stage('Build Docker Image') {
            steps {
                dockerBuildImage('azeyna/jma:3.0')
            }
        }

        stage('Push Docker Image') {
            steps {
                dockerPush('azeyna/jma:3.0')
            }
        }
    }
}
