@Library('jenkins-shared-library') _
pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                gitCheckout(
                    branch: 'master',
                    url: 'https://github.com/kulkarni-abhishek/spring-boot-jenkins.git'
                )
            }
        }

        stage('Gradle unit Test') {
            steps {
                gradleTest()
            }
        }

        stage('Gradle integration test') {
            steps {
                gradleIntTest()
            }
        }
    }
}